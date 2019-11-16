# Estructura modular en JS con Parcel para trabajar con servidores externos

La idea es tener un archivo principal JS que ejecuta funciones de inicialización dependiendo de la vista, ver el ejemplo en `src/index.js`.

Cada módulo exporta por default una función llamada `init`, que inicializa la funcionalidad contenida en ese módulo.

Nótese que el `index.html` llama a los archivos de `css` y `js` desde el directorio `dist`. Este directorio y estos archivos los crea `parcel` automáticamente.

## Setup y workflow
### Instalar parcel
```bash
# si no hay package.json
npm init

npm i parcel -D
```

### Iniciar compilador
Se usa el comando `parcel watch src/index.js` para compilar un archivo js con parcel y que se actualice automáticamente al salvar.

Para compilar una version para producción `parcel build src/index.js`

Se pueden crear aliases para estos comandos para que sea más fácil trabajar en equipo (ver el campo de `scripts` en el archivo `package.json`).


## Cómo probar este ejemplo
Para inciar `parcel`, en una terminal:

```bash
npm install

npm run dev
```

En otra terminal, para iniciar un servidor (usamos `python` pero puede ser cualquier otro servidor http).

```bash
python -m SimpleHTTPServer 8080
```