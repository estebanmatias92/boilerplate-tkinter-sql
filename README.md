# boilerplate-tkinter-sql

Plantilla base para crear desktop apps.

## Sinopsis de la app

Es un ejemplo de una app de escritorio, la idea es que actue como API cliente para la API de Spotify y traer la lista de canciones favoritas de tu cuenta de usuario.

- Tiene dos botones (Hello World y el Boton para traer la lista de cancioens)
- Ambos datos se deberian mostrar por ventana (Hello World funciona correctamente, la comunicacion con la API de spotify NO)
- En el archivo 'config.py' se debe cambiar las primeras 3 variables con los valores pertienentes

## Comunicacion con la API de Spotify

Para interactuar con la API de Spotify, necesitarás obtener un token de acceso. Este proceso implica registrar una aplicación en el [Dashboard de Desarrolladores](https://developer.spotify.com/dashboard/applications) de Spotify y utilizar las credenciales que obtienes para autenticar a tus usuarios y obtener el token.

#### Authentificacion

Puedes obtener estos valores de la siguiente manera:

- `SPOTIPY_CLIENT_ID` y `SPOTIPY_CLIENT_SECRET`: Obtienes estos al crear una nueva aplicación en tu panel de desarrolladores de Spotify. Una vez que se crea la aplicación, estos valores se mostrarán en la configuración de la aplicación.
- `SPOTIPY_REDIRECT_URI`: Esta es la URI a la que se redirigirá al usuario después de otorgar o negar el permiso a tu aplicación. Debe establecerse en una URI que tu aplicación pueda manejar y desde la cual pueda analizar el código de autorización. Para el desarrollo local, a menudo se puede [establecer](https://chat.openai.com/share/30ed012d-2289-4a9f-9a80-ccb70fdc58ca) en '<http://localhost:puerto/callback>', donde 'puerto' es un puerto abierto en tu máquina local. Asegúrate de agregar también esta URI a la lista de URIs de redireccionamiento en la configuración de tu aplicación en el panel de desarrolladores de Spotify.
- `SCOPE`: Esta es una cadena de caracteres separada por espacios que especifica los permisos que tu aplicación está solicitando. El ámbito `user-library-read`, por ejemplo, otorga a tu aplicación acceso de lectura a la biblioteca "Tu música" de un usuario. Otros ámbitos otorgan diferentes derechos de acceso. Puedes encontrar una lista de todos los ámbitos disponibles en la [documentación de ámbitos de autorización de Spotify](https://developer.spotify.com/documentation/general/guides/scopes/).

Recuerda reemplazar `'your-spotify-client-id'`, `'your-spotify-client-secret'` y `'your-app-redirect-url'` con los valores reales que obtienes o decides.

Recuerda que el usuario debe estar registrado y debe otorgar a tu aplicación permiso para acceder a los datos según lo especificado por el `SCOPE`.

## Instalacion

Deben instalar desde la consola la libreria Pygame (asegurense de tener actualizado PIP)

```bash
pip install -Ur .\requirements.txt 
```

- En el archivo 'requirements.txt' se encuentran la libreria slistadas

## Scaffolding (organizacion de carpetas)

```bash
.
├───.gitignore
├───config.py
├───main.py
├───README.md
└───requirements.txt
```

## Uso

Como cualquier script o programa de python.

```bash
python "main.py"
```

*Para correrlo sin mencionar el directorio, la consola debe estar posicionada sobre la carpeta del proyecto.
