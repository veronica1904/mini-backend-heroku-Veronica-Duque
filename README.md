# mini-backend-heroku-Veronica-


Url API Fake: https://minibackend-veronica-duque.herokuapp.com/data/

Pasos para crear una Api fake con Heroku: 

1. Tener una cuenta en heroku para realizar la configuracion.
1.1. app new, colocamos el nombre deseado (create app)
1.2. luego de creada
3. en nuestro escritorio creamos una carpeta
4. dentro de ella abrimos visual studio 
5. luego en visual abrimos la terminal 
6. ejecuatamos el siguiente comando: npm init -Y 
7. luego que se crea nuestro package-json 
7.1. agregar la siguiente linea:  "start": "node server.js"
9. vamos a ejecutar el siguiente comando: npm install json-server
10. se me crea el node_module y package-lock-json
11. luego creamos un archivo que va a tener nuestra data (data.json) nombre deseado.json
12. allí vamos a colocar nuestro objeto de nuestra data 
13. luego creamo nuestro archivo serve.js que se hace para levantar un servidor 
14. colocar lo siguiente en server.js :

const jsonserver = require('json-server');
const server = jsonserver.create();
const router = jsonserver.router('backendveronicaduque.json');
const middlewares = jsonserver.defaults();

server.use(middlewares);
server.use(router);
const port = process.env.PORT || 4000;
server.listen(port, () => {
    console.log('JSON Server is running');
})

15. cuando corremos con npm start, debe aparecer JSON Server is running
16. luego abrimos una consola de gitbash para hacer las configuraciones de heroku que nos da cuando creamos la nueva app. 
