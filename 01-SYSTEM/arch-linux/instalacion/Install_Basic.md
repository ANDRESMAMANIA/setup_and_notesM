> [!Nota importante]  
> El ecosistema de software evoluciona constantemente. En caso de que algún paquete o comando ya no funcione debido a que los nombres cambiaron o el programa quedó obsoleto, se recomienda consultar con una Inteligencia Artificial actualizada o revisar los repositorios oficiales y el AUR.
---

## 1. Actualización Primordial del Sistema

Antes de proceder con la instalación de cualquier software o herramienta adicional, es obligatorio asegurarse de que todo el sistema base se encuentre completamente actualizado. Esto previene conflictos de dependencias rotas en entornos de actualización continua (*rolling release*).

Archivo generado exitosamente en: Guia_Post_Instalacion_Arch_Linux.md
```bash
sudo pacman -Syu
````
## 2. Instalación del Helper de AUR: YAY

Muchos de los paquetes avanzados o de terceros no se encuentran en los repositorios oficiales de Arch Linux, sino en el Repositorio de Usuarios de Arch (AUR). Para gestionarlos de forma automatizada, se utiliza `yay`.

Para que el gestor verifique si las dependencias base ya se encuentran en el sistema y omita su descarga en ese caso, se implementa el parámetro `--needed`. Toda esta secuencia se debe ejecutar mediante la terminal como usuario normal (no como _root_).

**Paso 1: Instalar dependencias de compilación y control de versiones**
```bash
sudo pacman -S --needed base-devel git
```

**Paso 2: Clonar el repositorio oficial de YAY**
```bash
git clone [https://aur.archlinux.org/yay.git](https://aur.archlinux.org/yay.git)
```

**Paso 3: Acceder al directorio clonado**
```bash
cd yay
```

**Paso 4: Compilar e instalar el paquete**
```bash
makepkg -si
```

Con este último comando se genera el binario y se instala en el sistema, habilitando una biblioteca de herramientas y programas sin las restricciones del catálogo de `pacman` convencional.

## 3. Ofimática y Gestión de PDF

### Suites Ofimáticas

- **libreoffice-still**: Representa la rama con soporte a largo plazo de la suite. Ha pasado por múltiples revisiones de errores, garantizando estabilidad absoluta y madurez en la compatibilidad con formatos estándar (`.docx`, `.xlsx`, `.pdf`).
    
- **libreoffice-still-es**: Paquete de localización que traduce la interfaz gráfica completa al español (menús, herramientas y ayuda local) acoplándose a la configuración regional.
    
- **Diccionarios de corrección ortográfica**: `hunspell-es_cl` (adaptado con modismos y términos técnicos de Chile) y `hunspell-es_es` (castellano estándar).
    
```bash
sudo pacman -S --needed libreoffice-still libreoffice-still-es hunspell-es_cl hunspell-es_es hunspell hunspell-es_any
```

- **onlyoffice-bin**: Suite orientada a la nube y al trabajo colaborativo. El sufijo `-bin` indica que descarga el binario precompilado desde el AUR, evitando tiempos prolongados de compilación en el procesador.
    
- **wps-office**: Alternativa privativa (_freeware_) que ofrece una de las reproducciones más fieles y exactas de la interfaz "Ribbon" de Microsoft Office.
    
```bash
yay -S --needed onlyoffice-bin wps-office
```

### Visores y Editores de PDF

- **okular**: Visor universal desarrollado por KDE. Soporta anotaciones avanzadas, resaltado, notas adhesivas, firmas digitales y lectura de formatos adicionales como EPUB, imágenes y cómics.
    
- **evince**: El visor oficial de GNOME, enfocado en el minimalismo, velocidad y bajo consumo de recursos.
    
```bash
sudo pacman -S --needed okular evince
```

- **foxitreader**: Versión para Linux del clásico software comercial, rápido en renderizado y óptimo para rellenar formularios complejos.
    
- **masterpdfeditor-free**: Herramienta potente para la edición real de documentos PDF. Permite modificar texto interno, mover imágenes, estructurar páginas y diseñar formularios. La versión _free_ cuenta con ciertas limitaciones operativas.
    
```bash
yay -S --needed foxitreader masterpdfeditor-free
```

## 4. Tipografía y Tipos de Fuentes

Para evitar problemas de renderizado o desconfiguración visual al abrir documentos creados en entornos de Microsoft Office, es indispensable añadir las familias tipográficas estándar.

```bash
sudo pacman -S --needed ttf-liberation ttf-dejavu
yay -S --needed ttf-ms-fonts
```

## 5. Particionado de Discos, Formatos y Controladores

### Soporte de Sistemas de Archivos

Este conjunto de paquetes habilita la compatibilidad con múltiples formatos de almacenamiento, permitiendo formatear y gestionar particiones específicas o comunes (como exFAT o NTFS) desde el sistema operativo.

```bash
sudo pacman -S --needed dosfstools ntfs-3g exfatprogs btrfs-progs xfsprogs f2fs-tools
```

### Conectividad con Dispositivos Android

Herramientas e implementaciones del protocolo MTP necesarias para garantizar la correcta comunicación, transferencia de archivos y asignación de reglas de dispositivos Android a través del bus USB.

```bash
sudo pacman -Syu --needed mtpfs libmtp gvfs-mtp gvfs-gphoto2 android-udev
```

## 6. Navegadores Web

Selección de navegadores adaptados a diferentes flujos de trabajo y requerimientos de privacidad.

### Desde Repositorios Oficiales (Pacman)

- **chromium**: Proyecto de código abierto base de Google Chrome, pero limpio de la telemetría propietaria. Mantenido activamente por la comunidad.
    

```bash
sudo pacman -Syu --needed chromium
```

_Si se prefiere instalar Chromium junto a Brave de manera simultánea:_

```bash
sudo pacman -Syu --needed brave chromium
```

### Desde AUR (Yay)

- **google-chrome**: El navegador oficial de Google. Mantiene la integración completa con su ecosistema, herramientas de sincronización nativas y servicios propietarios, incluyendo sus módulos de telemetría.
    
- **vivaldi**: Enfocado en la productividad y personalización exhaustiva, cuenta con bloqueadores integrados y ausencia de telemetría intrusiva. (Nota: Vivaldi está basado en Chromium).
    
- **brave-bin**: Centrado firmemente en la seguridad, bloqueando anuncios y rastreadores de forma nativa sin romper la experiencia web.
    
- **tor-browser**: Diseñado específicamente para preservar el anonimato en línea mediante el enrutamiento de la red Tor.
    

_Comando para compilar e instalar todas las opciones de AUR en una sola línea:_

```bash
yay -S --needed google-chrome vivaldi brave-bin tor-browser
```

## 7. Emuladores de Terminal

Optimización del entorno de línea de comandos mediante emuladores de alto rendimiento.

- **kitty**: Emulador de terminal avanzado que delega el renderizado de la interfaz directamente a la GPU, ofreciendo una latencia mínima y soporte para despliegue de imágenes.
    
- **alacritty**: Enfocado estrictamente en el rendimiento crudo y la simplicidad, configurado mediante archivos de texto plano sin añadidos innecesarios.
    

```bash
sudo pacman -Syu --needed alacritty kitty
```

## 8. Compresión y Descompresión de Archivos

### Gestión por Línea de Comandos

Formatos y algoritmos indispensables para el empaquetado y resguardo de datos.

- **7zip**: Sucesor moderno de `p7zip` en Arch. Ofrece tasas de compresión muy altas.
    
- **zstd**: Desarrollado por Meta, es el estándar de empaquetado en Arch Linux gracias a su velocidad en la descompresión.
    
- **xz**: Basado en LZMA2, ideal para almacenamiento a largo plazo (_cold storage_) por su óptimo ratio de reducción de espacio.
    

```bash
sudo pacman -S --needed 7zip zstd xz tar zip unzip
```

- **ouch**: Herramienta moderna escrita en Rust que simplifica la sintaxis. Detecta automáticamente las operaciones requeridas basándose en la extensión del archivo (ej. `ouch decompress archivo.tar.gz`).
    

```bash
sudo pacman -S --needed ouch
```

### Gestor Gráfico

- **peazip-qt-bin**: Alternativa de código abierto a WinRAR. Soporta más de 200 formatos y permite la conversión directa entre extensiones de compresión sin necesidad de una extracción intermedia previa.
    

```bash
yay -S --needed peazip-qt-bin
```

## 9. Aplicaciones de Cálculo y Entornos Matemáticos

- **cantor**: Front-end desarrollado por KDE que actúa como hoja de trabajo interactiva. Integra diferentes motores de cálculo para resolver ecuaciones y graficar.
    
    _(Nota: Se sugiere complementarlo con `maxima`, un potente sistema de álgebra computacional)._
    

```bash
sudo pacman -S --needed cantor maxima
```

- **qalculate-gtk**: Considerada una de las calculadoras de escritorio más completas. Entiende variables complejas, expresiones en lenguaje natural (ej. conversiones de divisas o constantes físicas) e incluye un amplio historial de operaciones.
    

```bash
sudo pacman -S --needed qalculate-gtk
```

_(Nota: Sustituir por `qalculate-qt` si se prefiere una mejor integración visual en entornos KDE)._

- **speedcrunch**: Diseñada para la ejecución veloz mediante el teclado. Ofrece una interfaz limpia, precisión arbitraria de cientos de decimales y una base de datos interna de constantes científicas.
    

```bash
sudo pacman -S --needed speedcrunch
```

- **kalgebra**: Enfocada en la representación gráfica analítica. Permite ingresar funciones matemáticas y proyectarlas instantáneamente en entornos bidimensionales (2D) y tridimensionales (3D).
    

```bash
sudo pacman -S --needed kalgebra
```

- **wxmaxima**: Interfaz gráfica para el motor CAS Maxima. Diseñada al estilo de un libro de texto conceptual, no se limita a entregar un resultado numérico, sino que expone el desarrollo simbólico de límites, derivadas e integrales.
    
```bash
sudo pacman -S --needed wxmaxima
```

- **geogebra**: Entorno dinámico y estándar educativo moderno. Reúne en una sola suite herramientas de geometría, álgebra, hojas de cálculo, gráficos 3D y estadística, respaldado por una amplia comunidad global.
    
```bash
sudo pacman -S --needed geogebra
```
