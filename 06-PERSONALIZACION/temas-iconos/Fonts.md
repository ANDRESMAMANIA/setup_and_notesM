En Linux, la mejor manera de mantener tus fuentes ordenadas (y separadas de las del sistema para que no se haga un desastre) es guardarlas en tu propia carpeta de usuario.

Como no quieres que esté todo mezclado ("chipado"), el truco está en **crear una carpeta dedicada para cada fuente** dentro del directorio oculto de fuentes de tu usuario (`~/.local/share/fonts`).

Aquí tienes el paso a paso exacto para hacerlo desde la terminal de forma ultra ordenada:

### Paso 1: Crear la estructura de carpetas

Primero, asegúrate de que exista el directorio de fuentes de tu usuario y luego crea una carpeta específica para la fuente que descargaste (por ejemplo, si bajaste _Hack_ o _JetBrainsMono_):
```bash
# Crear el directorio base de fuentes por si no existe
mkdir -p ~/.local/share/fonts

# Crear una carpeta limpia solo para tu nueva fuente (cambia "NombreDeLaFuente" por el que quieras)
mkdir -p ~/.local/share/fonts/NombreDeLaFuente
```

_(Por ejemplo: `mkdir -p ~/.local/share/fonts/JetBrainsMono`)_

### Paso 2: Descomprimir los archivos en su lugar

Normalmente, Nerd Fonts se descarga como un archivo `.zip`. Puedes mover ese `.zip` directamente a la carpeta que creaste y descomprimirlo ahí dentro para que todos los archivos `.ttf` o `.otf` queden guardados en su propio lugar.

Asumiendo que tu archivo se descargó en la carpeta `Downloads`, corre esto:
```bash
# Descomprimir el ZIP directamente en su carpeta correspondiente
unzip ~/Downloads/NombreDelArchivo.zip -d ~/.local/share/fonts/NombreDeLaFuente/
```

Si revisas con `ls ~/.local/share/fonts/`, verás que cada fuente que instales en el futuro tendrá su propia carpeta independiente. ¡Cero desorden!

### Paso 3: Limpiar el archivo ZIP viejo (Opcional)

Para no acumular basura en tu carpeta de descargas, borra el archivo comprimido que ya no usas:
```bash
rm ~/Downloads/NombreDelArchivo.zip
```

### Paso 4: Actualizar la caché de fuentes del sistema

Para que Linux y tu terminal se enteren de que hay una nueva fuente disponible en el equipo, ejecuta este comando obligatorio:
```bash
fc-cache -fv
```

### Paso 5: Verificar que Linux la reconoce

Si quieres asegurarte de que el sistema la detectó correctamente y ver el nombre exacto con el que se registró, ejecuta:
```bash
fc-list : family | grep -i "Nerd Font"
```
---
##### Recomendación
> Pagina para ver y descargar fuentes gratis:
> 
> ```bash
> https://www.nerdfonts.com/font-downloads
> ```
> 
