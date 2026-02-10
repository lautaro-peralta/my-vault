$改善 - Kaizen$

---
##  Facultad

> [!todo] Notas Pendientes Globales
> Esta base de datos centraliza todas tus `Rough Notes` con el estado `#pendiente`.
> 
> ![[pendientes_GLOBAL.base]]

---
## Personal

> [!abstract] Proyectos Activos 
> 
> **[[GarrSYS]]**
> 
> **[[Rome Fitness]]**
> 
> **[[Inventar3D]]**

---
## Entrenamiento

```dataviewjs
const hoy = dv.luxon.DateTime.now();
const inicioSemana = hoy.startOf('week'); 
const finSemana = hoy.endOf('week'); 
const sesionesObjetivo = 4;
const semanasAMostrar = 4;

// --- 1. PROCESAMIENTO DE DATOS PARA TABLA Y GRÁFICO ---
const todasLasNotas = dv.pages().where(p => p.Tipo && String(p.Tipo).includes("entrenamiento") && p.Fecha);

const entrenamientosEstaSemana = todasLasNotas
    .filter(p => {
        const dt = dv.luxon.DateTime.fromFormat(p.Fecha.toString(), "dd-MM-yyyy, HH:mm");
        return dt.isValid && dt >= inicioSemana && dt <= finSemana;
    })
    .array()
    .sort((a, b) => dv.luxon.DateTime.fromFormat(a.Fecha.toString(), "dd-MM-yyyy, HH:mm") - dv.luxon.DateTime.fromFormat(b.Fecha.toString(), "dd-MM-yyyy, HH:mm"));

// --- 2. RENDERIZADO DEL RESUMEN Y TABLA ---
const sesionesRealizadas = entrenamientosEstaSemana.length;
const porcentaje = Math.round((sesionesRealizadas / sesionesObjetivo) * 100);

dv.header(4, "Resumen Semanal");
dv.paragraph(`**Progreso actual:** ${sesionesRealizadas} / ${sesionesObjetivo} sesiones (${porcentaje}%)`);

if (sesionesRealizadas > 0) {
    let html = `<table class="dataview table-view-table" style="width: 100%;">
      <thead><tr><th>Fecha</th><th>Nota</th><th>Enfoque</th><th>Día</th></tr></thead>
      <tbody>`;
    for (let p of entrenamientosEstaSemana) {
        const dt = dv.luxon.DateTime.fromFormat(p.Fecha.toString(), "dd-MM-yyyy, HH:mm");
        html += `<tr>
          <td>${dt.toFormat("dd-MM-yyyy HH:mm")}</td>
          <td><a class="internal-link" href="${p.file.path}">${p.file.name}</a></td>
          <td>${p.Enfoque || "N/A"}</td>
          <td>${dt.setLocale('es').toLocaleString({ weekday: 'long' })}</td>
        </tr>`;
    }
    html += `</tbody></table>`;
    dv.el("div", html);
} else {
    dv.paragraph("⚠️ No hay sesiones registradas esta semana.");
}

dv.paragraph("---");

// --- 3. LÓGICA DEL GRÁFICO (OBSIDIAN CHARTS) ---
let etiquetas = [];
let datosRealizados = [];

for (let i = semanasAMostrar - 1; i >= 0; i--) {
    const inicioBusqueda = hoy.minus({ weeks: i }).startOf('week');
    const finBusqueda = hoy.minus({ weeks: i }).endOf('week');
    
    const cuenta = todasLasNotas.filter(p => {
        const dt = dv.luxon.DateTime.fromFormat(p.Fecha.toString(), "dd-MM-yyyy, HH:mm");
        return dt.isValid && dt >= inicioBusqueda && dt <= finBusqueda;
    }).length;

    etiquetas.push(i === 0 ? "Esta semana" : `Hace ${i} sem.`);
    datosRealizados.push(cuenta);
}

const chartData = {
    type: 'bar',
    data: {
        labels: etiquetas,
        datasets: [
            {
                label: 'Sesiones Realizadas',
                data: datosRealizados,
                backgroundColor: 'rgba(54, 162, 235, 0.5)',
                borderColor: 'rgba(54, 162, 235, 1)',
                borderWidth: 1
            },
            {
                label: 'Objetivo',
                data: Array(semanasAMostrar).fill(sesionesObjetivo),
                type: 'line',
                borderColor: 'rgba(255, 99, 132, 1)',
                borderWidth: 2,
                fill: false,
                pointRadius: 0
            }
        ]
    },
    options: {
        scales: { y: { beginAtZero: true, suggestedMax: 5, ticks: { stepSize: 1 } } }
    }
};

window.renderChart(chartData, this.container);
```


#### Progreso en PRs

```dataviewjs
// 1. Parámetros base y obtención del peso corporal dinámico
const registroPeso = dv.pages().where(p => p.Peso_Corporal).sort(p => p.Fecha || p.file.mday, 'desc').first();
const pesoActual = registroPeso ? Number(registroPeso.Peso_Corporal) : 92; 

const notas = dv.pages().where(p => p.Tipo && String(p.Tipo).includes("entrenamiento") && p.Fecha);

// 2. Función de cálculo 1RM Epley optimizada
const get1RM = (data, esDominada = false) => {
    if (!data || !Array.isArray(data)) return 0;
    let peso = Number(data[0]);
    let reps = Number(data[1]);
    if (esDominada) peso += pesoActual; 
    return peso * (36/ (37 - reps));
};

// 3. Configuración de ejercicios (He incluido los 5 originales de tu código)
const config = [
    { nombre: "Sentadilla", prop: "Sentadilla", dom: false },
    { nombre: "Press Inclinado", prop: "Press_Inclinado", dom: false },
    { nombre: "Dominadas", prop: "Dominadas", dom: true },
    { nombre: "Curl Bíceps", prop: "Curl_Biceps", dom: false },
    { nombre: "Vuelos Lat.", prop: "Vuelos_Laterales", dom: false }
];

// 4. Procesamiento de registros máximos
const filas = config.map(ej => {
    const notasConEj = notas.where(p => p[ej.prop]);
    if (notasConEj.length === 0) return [ej.nombre, "Sin datos", "-", "-"];
    
    const record = notasConEj.sort(p => get1RM(p[ej.prop], ej.dom), "desc").first();
    const valor1RM = get1RM(record[ej.prop], ej.dom).toFixed(2);
    const cargaReal = record[ej.prop][0];
    const repeticiones = record[ej.prop][1];

    // Simplificación: Tomamos solo el nombre del archivo sin el path
    const nombreNota = record.file.name; 

    return [
        `<b>${ej.nombre}</b>`,
        `<b>${valor1RM} kg</b>`,
        `${cargaReal}kg x ${repeticiones}`,
        `<a class="internal-link" href="${record.file.path}">${nombreNota}</a>`
    ];
});

// 5. Renderizado con estilo profesional y ancho completo
let html = `<table class="dataview table-view-table" style="width: 100%; font-size: 0.9em; border-collapse: collapse;">
    <thead>
        <tr style="border-bottom: 2px solid var(--background-modifier-border);">
            <th style="text-align: left; padding: 10px;">Ejercicio</th>
            <th style="text-align: left; padding: 10px;">PR (1RM)</th>
            <th style="text-align: left; padding: 10px;">Récord Real</th>
            <th style="text-align: left; padding: 10px;">Referencia</th>
        </tr>
    </thead>
    <tbody>`;

filas.forEach(f => {
    html += `<tr style="border-bottom: 1px solid var(--background-modifier-border-減); transition: background 0.2s;">
        <td style="padding: 8px 10px;">${f[0]}</td>
        <td style="padding: 8px 10px; color: #4bc0c0;">${f[1]}</td>
        <td style="padding: 8px 10px;">${f[2]}</td>
        <td style="padding: 8px 10px; font-size: 0.85em;">${f[3]}</td>
    </tr>`;
});

html += `</tbody></table>`;
dv.el("div", html);
```

```dataviewjs
// --- 1. PROCESAMIENTO DE DATOS Y PESO CORPORAL ---
const registroPeso = dv.pages().where(p => p.Peso_Corporal).sort(p => p.Fecha || p.file.mday, 'desc').first();
const ultimoPeso = registroPeso ? Number(registroPeso.Peso_Corporal) : 92; // Valor actual: 92kg

const notas = dv.pages().where(p => p.Tipo && String(p.Tipo).includes("entrenamiento") && p.Fecha);

// Fórmula de Epley: 1RM = Peso * (1 + Reps / 30)
const calcular1RM = (data, esCorporal = false) => {
    if (!data || !Array.isArray(data)) return 0;
    let pesoCarga = Number(data[0]);
    let reps = Number(data[1]);
    if (isNaN(pesoCarga) || isNaN(reps) || reps > 50) return 0; 

    let pesoTotal = esCorporal ? (pesoCarga + ultimoPeso) : pesoCarga;
    let resultado = pesoTotal * (36 / (37 - reps));
    return resultado > 1000 ? 0 : parseFloat(resultado.toFixed(2));
};

const notasValidas = notas.map(p => {
    const dt = dv.luxon.DateTime.fromFormat(p.Fecha.toString(), "dd-MM-yyyy, HH:mm");
    return { ...p, dt };
}).filter(p => p.dt.isValid);

const etiquetas = [...new Set(notasValidas.map(p => p.dt.toFormat("dd/MM")))].sort();

// --- 2. CONFIGURACIÓN DE CATEGORÍAS ---
const grupoPesado = [
    { label: 'Sentadilla', prop: 'Sentadilla', color: '#ff6384', corp: false },
    { label: 'Press Inclinado', prop: 'Press_Inclinado', color: '#36a2eb', corp: false },
    { label: 'Dominadas', prop: 'Dominadas', color: '#4bc0c0', corp: true },
    { label: 'Jalón Pecho', prop: 'Jalon_Pecho', color: '#ffcd56', corp: false },
    { label: 'Fondos', prop: 'Fondos', color: '#c9cbcf', corp: true }
];

const grupoAislamiento = [
    { label: 'Curl Bíceps', prop: 'Curl_Biceps', color: '#9966ff', corp: false },
    { label: 'Vuelos Lat.', prop: 'Vuelos_Laterales', color: '#ff9f40', corp: false },
    { label: 'Tríceps Polea', prop: 'Triceps_Polea', color: '#32a852', corp: false }
];

// --- 3. LÓGICA DE ESCALAMIENTO PROPORCIONAL (Padding 10%) ---
const obtenerLimites = (ejercicios) => {
    let valores = [];
    ejercicios.forEach(ej => {
        etiquetas.forEach(fecha => {
            const nota = notasValidas.find(p => p.dt.toFormat("dd/MM") === fecha && p[ej.prop]);
            if (nota) {
                const val = calcular1RM(nota[ej.prop], ej.corp);
                if (val > 0) valores.push(val);
            }
        });
    });
    if (valores.length === 0) return { min: 0, max: 100 };
    const minReal = Math.min(...valores);
    const maxReal = Math.max(...valores);
    // Aplicación de margen proporcional del 10%
    return { min: minReal * 0.9, max: maxReal * 1.1 };
};

// --- 4. RENDERIZADO ---
const crearConfig = (titulo, ejercicios) => {
    const limites = obtenerLimites(ejercicios);
    return {
        type: 'line',
        data: {
            labels: etiquetas,
            datasets: ejercicios.map(ej => ({
                label: ej.label,
                data: etiquetas.map(fecha => {
                    const nota = notasValidas.find(p => p.dt.toFormat("dd/MM") === fecha && p[ej.prop]);
                    return nota ? calcular1RM(nota[ej.prop], ej.corp) : null;
                }),
                borderColor: ej.color,
                spanGaps: true,
                tension: 0.3
            }))
        },
        options: {
            plugins: { title: { display: false } }, // Título minimalista fuera del gráfico
            scales: { 
                y: { 
                    min: Math.floor(limites.min),
                    max: Math.ceil(limites.max),
                    ticks: { precision: 0 }
                } 
            }
        }
    };
};

dv.header(4, "Rendimiento Multiarticular");
window.renderChart(crearConfig("Multi", grupoPesado), this.container);

dv.header(4, "Rendimiento de Aislamiento");
window.renderChart(crearConfig("Aislamiento", grupoAislamiento), this.container);
```



