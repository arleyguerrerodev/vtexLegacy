Documentación: https://tailwindcss.com/docs/installation/using-postcss

>>Iniciar proyecto npm: npm init

>>Instalar Tailwind como un plugin de PostCSS:
    npm install -D tailwindcss postcss autoprefixer

>>Se ejecuta el siguiente comando:
    npx tailwindcss init ->  Para crear el archivo "tailwind.config.js" colocando la siguiente configuración:
        module.exports = {
        content: ["./public/index.html", "./src/**/*.{html,js}"], -> Lugar en el que va a revisar en donde estamos creando las clases css desde npm
        theme: {
            extend: {},
        },
        plugins: [],
        };

>>Incluir Tailwind en el CSS agregando las directivas a src/css/tailwind.css:
    @tailwind base;
    @tailwind components;
    @tailwind utilities;

>>Para correr los estilos de Tailwind se ejecuta el siguiente comando:
    npx tailwindcss -i ./src/css/tailwind.css -o ./public/css/tailwind.css --watch

    Indicamos que nuestro archivo tailwind.css que proviene de src haga un build en la carpeta de public al archivo tailwind.css.