![svelte library app](https://user-images.githubusercontent.com/13697123/82756260-c1339c00-9d9e-11ea-87e0-fe4c3cd33777.PNG)

# Aplicación de biblioteca Svelte

Este es un proyecto simple de una aplicación de biblioteca donde puede almacenar libros en una base de datos falsa local (db.json), en general, aprendí conceptos básicos de componentes esbeltos, interfaces de usuario de interactividad y vincular datos de formularios. Este proyecto es parte del aprendizaje con fines educativos

![svelte library app responsive](https://user-images.githubusercontent.com/13697123/82756905-9fd4af00-9da2-11ea-9dc5-35cf66e4c851.PNG)


## Empezamos con la Instalacion de Dependencias

En la terminal  debemos ingresar a la carpeta y ejecutar el comando para instalar todas las dependencias para que el sistema funcione


Comandos para llevarlo acabo acontinuacion:
```bash
cd library-svelte-app
npm install
```

...A continuacion inicie el paquete administrativo [Rollup](https://rollupjs.org):

```bash
npm run dev
```
Navege a la dirreccion  [localhost:5000](http://localhost:5000).Deberías ver tu aplicación ejecutándose. Edite un archivo de componente en `src`, guárdelo y vuelva a cargar la página para ver sus cambios.

De forma predeterminada, el servidor solo responderá a las solicitudes de localhost. Para permitir conexiones desde otras computadoras, edite los comandos `sirv` en package.json para incluir la opción `--host 0.0.0.0`.


## Construir y ejecutar en modo de producción

Para crear una versión optimizada de la aplicación:
Comandos para llevarlo acabo a continuacion:
```bash
npm run build
```

Puede ejecutar la aplicación recién creada con `npm run start`. Esto usa [sirv](https://github.com/lukeed/sirv), que está incluido en las `dependencias` de tu paquete.json para que la aplicación funcione cuando la implementes en plataformas como [Heroku](https:// heroku.com).

## Modo de aplicación de una sola página
Por defecto, sirv solo responderá a las solicitudes que coincidan con los archivos en `público`. Esto es para maximizar la compatibilidad con servidores de archivos estáticos, lo que le permite implementar su aplicación en cualquier lugar.

Si está creando una aplicación de una sola página (SPA) con varias rutas, sirv debe poder responder a las solicitudes de *cualquier* ruta. Puede hacerlo editando el comando `"start"` en package.json:

```js
"start": "sirv public --single"
```


## Implementación en la web

### Con [now](https://zeit.co/now)

Instala `now` si aún no lo has hecho:
```bash
npm install -g now
```
Luego, desde dentro de la carpeta de su proyecto:

```bash
cd public
now deploy --name my-project
```

Como alternativa, utilice el [Now desktop client](https://zeit.co/download) y simplemente arrastre la carpeta del proyecto descomprimida al icono de la barra de tareas.

### con [surge](https://surge.sh/)

Instale `surge` si aún no lo has hecho:

```bash
npm install -g surge
```
Luego, desde dentro de la carpeta de su proyecto:

```bash
npm run build
surge public my-project.surge.sh
```
