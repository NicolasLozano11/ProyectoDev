# CIA ®2.0 (Central de información actualizada)

La plataforma CIA®2.0, es una versión actualizada de la plataforma CIA 1.0, representa el avance tecnológico en Cosinte Ltda. Proporciona servicios importantes en análisis, inteligencia, operaciones e investigaciones. Adicionalmente CIA®2.0 ofrece a los equipos gerenciales herramientas estadísticas avanzadas, gráficas y métricas de rendimiento que proveen información valiosa para la toma de decisiones. El sistema es principalmente utilizado por investigadores y analistas de campo, quienes lo encuentran un aliado esencial en la gestión de información crítica de manera eficiente, sin embargo, tiene un alcance global dentro de los diferentes departamentos de Cosinte, así como en la administración de relaciones con el cliente.

## Características

- Solicitud y gestión de procesos de naturaleza operativa.
- Generación de reportes e informes. 
- Gestión documental.

## Tecnologías

La plataforma utiliza las siguientes dependencias para funcionar correctamente:

- **[React]** - Biblioteca para interfaces de usuario web y nativas.
- **[Redux]** - Contenedor predecible del estado de aplicaciones JavaScript.
- **[Bootstrap]** - Kit de herramientas de interfaz de usuario (Layout).
- **[Material UI]** - Biblioteca de herramientas de interfaz de usuario personalizable.
- **[React Router]** - Biblioteca de enrutamiento del lado del cliente.
- **[Recharts]** - Biblioteca de gráficos.
- **[i18next]** - Marco de internacionalización (soporte de múltiples idiomas)
- **[React Hook Form]** - Biblioteca para manejo de formularios y validación.

> Anteriormente se listan las dependencias que se utilizan de maneral global o tienen un impacto significativo dentro del sistema, sin embargo el proyecto dispone de una extensa lista de bibliotecas que se utilizan para funcionalidades específicas.
 
## APIs

| API | Descripción | Documentación |
| ------ | ------ | ------ |
| CIA backend | Lógica del negocio (php) | [Docs][PlDb] |
| Maps JavaScript API | Renderización de mapas |[Docs][PlGh] |
| Geocoding API | Marcadores de mapa y direcciones| [Docs][PlGd] |
| reCAPTCHA v2 | Marcadores de mapa y direcciones| [Docs][PlOd] |
 
 
## Requisitos 

Para ambientes de desarrollo:

- Entorno de ejecución **[Node.js](https://nodejs.org/)** v17.0.0+ 

## Instalación

Descargue el proyecto desde GitHub: 

```bash
git clone https://github.com/COSINTEDEV/ciaV2
cd ciaV2
```

> Tenga en cuenta que el repositorio es privado, lo que significa que requerirá que las credenciales de autenticación de github dentro de su sistema se encuentren en la lista de usuarios permitidos del repositorio remoto.

Para ejecutar el proyecto en su máquina: 

1. Instale las dependencias.
    ```sh
    npm install
    ```
    > Si tiene problemas con la instalción utilice la bandera `--force`, tenga en cuenta que lo anterior puede tener consecuencias imprevistas, ya que ignora los controles de seguridad y puede resultar en la instalación de paquetes no deseados o incompatibles. 
    
2. Inicialice el servidor.
    ```sh
    npm start
    ```

## Despliegue

Para despliegue en entornos de producción:

```sh
npm run build
```

Este comando ejecutará la instrucción:

```sh
react-scripts --openssl-legacy-provider --max_old_space_size=8192 build 
```

Donde:

- **--openssl-legacy-provider** : Hace que Node.js utilice la implementación "legacy" de OpenSSL para ciertas operaciones criptográficas, en lugar de la implementación "predeterminada". Se requiere su utilización para evitar errores de compatibilidad con la versión de Node.js instalada en el equipo que ejecuta el comando.
- **--max_old_space_size=8192** : Establece el tamaño máximo del espacio de memoria para objetos antiguos a 8192 megabytes, o 8 gigabytes, para evitar errores de falta de memoria en el heap de JavaScript. Se debe ajustar acorde a las capacidades de memoria RAM del equipo que ejecuta el comando.

> Los archivos compilados resultado del proceso de construcción se encuentran disponibles en la carpeta `build` dentro de la raíz del proyecto, y se actualizarán cada vez que ejecute el comando.

## Depuración de archivos

Para el depliegue en la infraestructura específica de Cosinte Ltda, se realiza un proceso previo de depuración, que incluye la modificación manual de los archivos **asset-manifest.json** e **index.html** (carpeta build).
Para facilitar dicho proceso se recomienda utilizar el script automatizado que se encuentra en la raíz del proyecto:

```sh
./deploy.sh
```

> El anterior script compilará el proyecto y depurara los archivos automáticamente. Los archivos listos para su despliegue en producción se encuentran disponibles en la carpeta `build` dentro de la raíz del proyecto, y se actualizarán cada vez que ejecute el comando.

## Licencia

© 2023 - Todos los derechos reservados - COSINTE LTDA

[//]: # (Estos son enlaces de referencia utilizados en el cuerpo de esta nota y se eliminan cuando el procesador de rebajas hace su trabajo. No es necesario darle un buen formato porque no debería verse - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [React]: <https://es.react.dev/reference/react>
   [Redux]: <https://es.redux.js.org/>
   [Bootstrap]: <https://getbootstrap.com/docs/4.6/getting-started/introduction/>
   [Material UI]: <https://v4.mui.com/getting-started/installation/>
   [React Router]: <https://v5.reactrouter.com/web/guides/quick-start>
   [Recharts]: <https://recharts.org/en-US/api>
   [i18next]: <https://react.i18next.com/>
   [React Hook Form]: <hhttps://react-hook-form.com/docs>

   [PlDb]: <>
   [PlGh]: <https://developers.google.com/maps/documentation/javascript?hl=es-419>
   [PlGd]: <https://developers.google.com/maps/documentation/geocoding?hl=es-419>
   [PlOd]: <https://developers.google.com/recaptcha/docs/display?hl=es-419>
