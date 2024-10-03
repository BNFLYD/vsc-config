# Personalizacion de VS Code

Esto es una personalizacion minimalista de VS Code.

## Extenciones necesarias

* Custom CSS and JS Loader (be5invis.vscode-custom-css)
* Material Theme
* Material Icon Theme

## Inicialización del proyecto

### 1. Clonar el repositorio

Clona el repositorio en tu máquina local ejecutando el siguiente comando en la terminal:

```bash
git clone https://github.com/tu-usuario/vsc-config.git
```

### 2. Instalar las extenciones de VS Code
Instala las extenciones mencionadas en un principio en tu VS Code

### 3. Configurar las opciones de usuario
Abri el archivo de opciones de usuario de VS Code apretando Ctrl + Shift + P y busca las opciones de usuario

```bash
Preferences: Open User Settings (JSON)
```

Una vez dentro del archivo copia el archivo del repositorio llamado settings.json

### 4. Importar los archivos css y js a las opciones de usuario
Segun la ruta donde tengas alojada la carpeta del repositorio importa los archivos usando la ruta cruda modificando los imports del principio del archivo settings.json por ejemplo:

```json
{
  //impotacion de archivos
  "vscode_custom_css.imports": [
    "file:///F:/repos/vsc-config/vscode-styles.css",
    "file:///F:/repos/vsc-config/blur.js"
  ],
}
```
Para obtener la ruta cruda de tu carpeta podes dirigirte a tu carpeta abrir una terminal desde ahi y ejecutar el siguiente comando:
```bash
pwd
```

### 5. Habilitar las personalizaciones
Una vez importados los archivos se deben habilitar las modificaciones de CSS y JS para esto debemos buscar la opcion apretando Ctrl + Shift + P y buscandola

```bash
Enable Custom CSS and JS
```

### 6. Recargar las personalizaciones
Ahora debemos reiniciar el editor para visualizar  las modificaciones de CSS y JS para esto debemos buscar la opcion apretando Ctrl + Shift + P y buscandola

```bash
Reload Custom CSS and JS
```
Con eso estaria, cada vez que hagamos alguna modificaion al archivo CSS o JS debemos recargar las personalizaciones.

### Herramientas utiles
Para cambiar el arte del inicio pueden crear un archivo svg de lo que quieran usando herramientas como https://excalidraw.com/ y luego arrastrar el archivo a VS Code para visualizar el codigo apretar Ctrl + A para seleccionarlo todo, copiarlo y pegarlo en un conversor de SVG a CSS como https://bloggerpilot.com/en/tools/svg-to-css/ para obtener el background-image y pegarlo en el archivo CSS remplazando la imagen por defecto del proyecto.

```css
/* arte svg personalizado */
.letterpress {
  background-image: url("tu arte svg va aca") !important;
  background-repeat: no-repeat no-repeat !important;
  background-position: center center !important;
  background-size: cover !important;
  background-size: contain !important;
  width: 60% !important;
  }
```

Es importante que despues de pegar tu background-image añadas las lineas "!important;" porque de lo contrario vas a estar mostrando la imagen por defecto del editor.

Una vez hecho esto podes recargar las personalizaciones para ver los cambios.
