# Estructura de Carpetas para Setup & Notes

```bash
├── 00-INDEX
│   ├── guia-rapida.md
│   └── mapa-general.md
├── 01-SYSTEM
│   ├── arch-linux
│   │   ├── instalacion
│   │   │   └── Install_Basic.md
│   │   ├── mantenimiento
│   │   ├── post-instalacion
│   │   └── troubleshooting
│   ├── boot-kernel
│   │   ├── grub.md
│   │   ├── kernel-params.md
│   │   └── systemd-boot.md
│   └── drivers-hardware
│       ├── audio.md
│       ├── bluetooth.md
│       ├── gpu.md
│       └── impresoras.md
├── 02-TERMINAL
│   ├── comandos
│   │   ├── avanzados.md
│   │   ├── basicos.md
│   │   ├── network.md
│   │   ├── system-admin.md
│   │   └── text-processing.md
│   ├── emuladores
│   │   ├── alacritty
│   │   ├── kitty
│   │   │   ├── atajos.md
│   │   │   ├── fuentes.md
│   │   │   ├── kitty.conf
│   │   │   ├── README.md
│   │   │   └── temas.md
│   │   ├── terminator
│   │   └── tmux
│   └── shells
│       ├── bash
│       │   ├── aliases.md
│       │   ├── bashrc.md
│       │   └── scripts
│       └── zsh
│           ├── aliases.md
│           ├── oh-my-zsh.md
│           ├── plugins.md
│           ├── themes.md
│           └── zshrc.md
├── 03-DESARROLLO
│   ├── editores-ide
│   │   ├── intellij
│   │   ├── neovim
│   │   ├── vim
│   │   └── vscode
│   │       ├── atajos.md
│   │       ├── extensions.md
│   │       ├── settings.json
│   │       └── snippets
│   ├── entornos
│   │   ├── java-jdk.md
│   │   ├── nodejs.md
│   │   ├── python-venv.md
│   │   └── variables-entorno.md
│   ├── herramientas
│   │   ├── databases
│   │   ├── docker
│   │   ├── git
│   │   │   ├── GIT_CONFIG.md
│   │   │   └── gitconfig.txt
│   │   └── kubernetes
│   └── lenguajes
│       ├── c-cpp
│       ├── java
│       ├── javascript
│       ├── python
│       │   ├── librerias.md
│       │   ├── setup.md
│       │   └── snippets
│       └── rust
├── 04-REDES
│   ├── conceptos
│   │   ├── modelos-osi-tcpip.md
│   │   ├── protocolos.md
│   │   └── subnetting.md
│   ├── configuracion
│   │   ├── dns.md
│   │   ├── firewall.md
│   │   ├── ip-estatica.md
│   │   └── network-manager.md
│   ├── herramientas
│   │   ├── netcat.md
│   │   ├── nmap.md
│   │   ├── tcpdump.md
│   │   └── wireshark.md
│   └── servicios
│       ├── apache-nginx.md
│       ├── ftp-sftp.md
│       ├── ssh.md
│       └── vpn.md
├── 05-SEGURIDAD
│   ├── fundamentos
│   │   ├── autenticacion.md
│   │   ├── certificados-ssl.md
│   │   └── criptografia.md
│   ├── herramientas
│   │   ├── fail2ban.md
│   │   ├── firewalld-ufw.md
│   │   ├── gpg.md
│   │   └── ssh-keys.md
│   └── practicas
│       ├── backup-seguro.md
│       ├── hardening-linux.md
│       └── permisos.md
├── 06-PERSONALIZACION
│   ├── dotfiles
│   │   ├── backup-dotfiles.md
│   │   └── gestion-dotfiles.md
│   ├── entorno-grafico
│   │   ├── componentes
│   │   │   ├── dunst.md
│   │   │   ├── picom.md
│   │   │   ├── polybar.md
│   │   │   └── rofi.md
│   │   ├── desktop-environments
│   │   │   ├── gnome
│   │   │   ├── kde
│   │   │   └── xfce
│   │   └── window-managers
│   │       ├── awesome
│   │       ├── bspwm
│   │       └── i3
│   └── temas-iconos
│       ├── cursores.md
│       ├── Fonts.md
│       ├── gtk-themes.md
│       └── icon-packs.md
├── 07-CARRERA
│   ├── informatica
│   │   ├── ia-machine-learning
│   │   ├── ingenieria-software
│   │   └── teoria-computacion
│   ├── ingenieria-sistemas
│   │   ├── algoritmos
│   │   ├── arquitectura-computadores
│   │   ├── bases-datos
│   │   └── sistemas-operativos
│   ├── proyectos
│   │   ├── proyecto-1
│   │   ├── proyecto-2
│   │   └── templates
│   └── redes
│       ├── fundamentos
│       ├── practicas-labs
│       ├── routing-switching
│       └── seguridad-redes
├── 08-CURSOS
│   ├── completados
│   │   └── [nombre-curso]
│   ├── en-progreso
│   │   └── [nombre-curso]
│   │       ├── codigo
│   │       ├── notas
│   │       └── recursos
│   └── pendientes
│       └── lista-cursos.md
├── 09-SCRIPTS
│   ├── automatizacion
│   ├── bash
│   ├── python
│   └── utilidades
├── 10-CHEATSHEETS
│   ├── docker-cheatsheet.md
│   ├── git-cheatsheet.md
│   ├── linux-commands.md
│   ├── network-commands.md
│   ├── shortcuts-globales.md
│   └── vim-cheatsheet.md
├── 11-RECURSOS
│   ├── documentacion
│   ├── enlaces-utiles
│   ├── libros
│   └── videos-tutoriales
├── 12-TEMPLATES
│   ├── template-config.conf
│   ├── template-documentacion.md
│   ├── template-readme.md
│   └── template-script.sh
├── 13.SOFTWARE
│   ├── CLI
│   ├── GUI
│   └── servicio
├── 14.INFRAESTRUCTURA
│   ├── contenedores
│   ├── diagramas
│   ├── homelab
│   ├── servidores
│   └── virtualizacion
├── 15.DIAGRAMAS
├── 16.WORKFLOWS
├── 17.LOGBOOK
│   └── 2026-07-05.md
├── LICENSE
└── README.md
```

## Estructura del Repositorio

Para que no te pierdas, organicé el contenido de la siguiente manera:

- **`00-INDEX/`**: El punto de partida. Guías rápidas de uso.
- **`01-SYSTEM/` & `02-TERMINAL/`**: Todo sobre la instalación de Arch, drivers, comandos de consola y la configuración de mi Shell (Zsh/Bash) y emulador de terminal (Kitty/Alacritty).
- **`03-DESARROLLO/`**: Mis entornos de programación (Python, Node.js, Java) y configs de editores (VS Code, Neovim).
- **`04-REDES/` & `05-SEGURIDAD/`**: Conceptos teóricos, protocolos, herramientas de análisis (Nmap, Wireshark) y buenas prácticas de hardening.
- **`06-PERSONALIZACION/`**: Mis archivos de configuración (_dotfiles_), temas, iconos y entornos visuales (i3, bspwm).
- **`07-CARRERA/` & `08-CURSOS/`**: Mi progreso académico, materias de ingeniería y cursos autodidactas.
- **`09-SCRIPTS/`**: Automatizaciones que me hacen la vida más fácil.
- **`10-CHEATSHEETS/`**: Recordatorios rápidos para cuando me falla la memoria.
- **`11-RECURSOS/` a `17-LOGBOOK/`**: Libros, plantillas reutilizables, software recomendado, diagramas de infraestructura y mi diario de aprendizaje diario (_logbook_).