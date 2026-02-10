15-09-2025, 11:23

Tags: [[Desarrollo de Software]]

---

Es un framework de nodejs, fue uno de los primeros , uno de los mas utilizados. Es utilizado por otros para poder extenderlo con mejores practicas, es unopinionated, lo hace versátil y ligero. Su idea es crear apps grandes sin agregar nuevos módulos. Es utilizado para por herramientas de front tamb. Entre los stackks, MEAN o MERN. Debido a su amplia utliizacion, aprender express sirve como base para aprender a usar muchas de las herramientas de js más modernas.
Herramientas
- principal: nodejs. Express esta Basado en nodejs (superior a la 14)
- Editor de codigo (vs code, codium, etc)
- git scm
Ya con esto se puede empezar.

Con express Estamos desarrollando apps backend. Modelos cliente servidor. 
Protocolo HTTP para comunicar a cliente con server. El cliente le hace una petición(request) el servidor procesa y retorna una respuesta(response). En la practica tenemos que crear a ambos. El cliente es mas de front, el server se puede crear con diff leng de programación. En este caso es con nodejs, con cod puro es muy trabajoso. Para desarrollar más rápido y escalabilidad, usamos express.

HTTP vs Express
Cuando el proyecto va creciendo, express es mucho mas útil comparado a solo node. 

Se usan los endpoints. Express

**Routing**

Servidor con distintas rutas. Podemos diseñar la app para que mediante diferentes direcciones url, nos muestre disntintos paneles, recursos, datos.
(Routes)
Es muy importante los tipos dentro de las responses a los clientes.
Nos permite extender nuestra app.
Si se visita una ruta no creada, express devuelve un msj 404, un ESTADO. 
Si quiero crear una ruta para que siempre responda lo mismo: app.use.

**HTTP Methods**

Funciones:
Get: pedir, obtener algo.
Post: lo contrario a get, el cli le manda datos al server y se guarda en el server.
Put: el cli quiere actualizar algún dato o recurso.
Patch, actualización parcial.
Delete: el cli quiere eliminar un recurso.

Estos verbos HTTP.
Sirven para dar info adicional.

Estas operaciones forman los CRUD.

Se usan los clientes rest para probar las rutas.

Se envian y reciben objetos JSON para hacer peticiones a los servers y para las responses.

Se pueden devolver solo los status.

**REQUEST BODY**

Asi como el server puede responder al cli,tambien el cli puede enviarle datos: JSON, form, etc.

Cliente envía objetos JSON:
Body: hay distintas pestañas.

Cuando enviamos una petición, se envía un documento que especifica le petición. Tiene un contenido y aparte tiene cabeceras para dar info de lo que se esta enviando.. REQUEST sirve para resumir este uso de documentos.
Contiene endpoints, body, data, y un header(JSON, por ej). Puede tener mas info.

Para la response, aplica lo mismo.

Tambien podemos poner codigo de estado (en el header)

Por ej: `console.log(req.body)` 
nos muesta el contenido de la REQUEST (body)
Se usa: `app.use(express.json())`  para que express entienda como manejar los objetos JSON.  Lo mismo para texto, urlencoded con extended: false (para forms), y más.

**REQUEST PARAMS**.

Los PARAMS se colocan en la URL, ''/hello/:username" por ejemplo:
`console.log(req.params.username)`

Se pueden usar parse para convertir strings a number.


'/hello/:x/:y"
`console.log(req.params.x)`
`console.log(req.params.y)`
Tambien  se puede hacer: `const {x,y} = req.params`

La ruta debe coincidir directamente.
Tambien se pueden retornar archivos

Se pueden hacer queries
/Blabla/search?user=Juan&age=20
Se usa en APIs para poder cambiar de paginas. ?page=2, ?page=3, etc para mostrar unos tantos recursos , en vez de todos de una. Por ej. Cuando buscas algo por MercadoLibre

Método all, para  poder enviar cualquiera de las peticiones

**INTRODUCCIÓN A  MIDDLEWARES**

Logging mediante funciones logger (que son middlewares).
Se ejecutan funciones antes de acceder a la ruta.
Se usa  `app.use`. Si lo dejas vacío, se ejecuta para todas las rutas
El parámetro next es una función para indicar que termino el trabajo de una función y para que se continue con el flujo normal.

**THIRD PARTY MIDDLEWARES**

se pueden instalar paquetes con middlewares. 

Middleware útil: Morgan para logs. morgan('dev'), morgan('tiny'),, morgan()

REST API

Servidor con ciertas URL que nos permiten procesar datos. Bajo ciertas recomendaciones.

REST API CRUD

Methods
De arreglos: push,find, filter, map,etc Luego estos se reemplazan con la implementación de las Bases de Datos.

Map:
productos.map(p => p.id === parseInt(req.params.id) ? { ...p, ...newData }:p)

Recorre el arreglo de productos, compara el ID de cada uno, con el que viene en PARAMS. Si es igual, se actualizan los valores. Si no, se conserva el producto

EXPRESS SETTINGS

Nombre de variable y su valor: 
app.set('appName', 'ExpressApp')
Case sensitive routing

STATIC FILES

Se pueden crear carpetas static o public, con archivos públicos que pueden ser accedidos mediante el navegador
app.use('/public', express.static('./public') )

Exite l modulo path para concatenar directorios, ya que express siempre considera que los archivos estan en el dir raíz. Con node, tenemos una cte llama ____dirname: la ruta absoluta.

app.use('/public',( express.static( path.join( __dirname, 'public' )))

























---
## Referencias