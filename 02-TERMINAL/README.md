#  Terminal
> [!Información]
> Una **shell** es, en esencia, la interfaz de texto que te permite interactuar con el sistema operativo. Actúa como un intérprete: toma los comandos que escribes en el teclado, los traduce y le dice al núcleo del sistema (el kernel) exactamente qué tiene que hacer. Cuando abres la terminal en tu sistema, lo que ves parpadeando y esperando tus órdenes es la shell.

## **Configuración de la terminal**
**ZSH**, también llamado **Z shell**, es una versión extendida de **Bourne Shell** (**sh**), con muchas características nuevas y soporte para plugins y temas. Dado que se basa en el mismo shell que **Bash**, **ZSH** tiene muchas de las mismas características. Empezar a utilizarlo es muy sencillo.

Se va a cambiar el **Shell** por uno mejor ya que se usa el nativo que es **bash** y en ves de eso vamos a usar el mas completo y actualizado que es **zsh**
Instalar zsh
```bash
sudo pacman -Syu --needed zsh
```
>Lo siguiente es verificar si  se instalo correctamente
>```bash
>zsh --version
>```
>ver los **Shell** disponible con el siguiente comando:
>```bash
>cat /etc/shells 
>```

Toca cambiar de Shell (de **bash a zsh** o viceversa) con lo siguiente :
```bash
chsh -s /bin/zsh
```  

**Verificar** :
```bash
echo $SHELL
```

>[!IMPORTANTE]
El cambio se aplicara al volver a iniciar sesión o reiniciar el equipo.

Para instalar y agregar pluguins acceder [AQUI](shells/zsh/plugins.md)
Para acceder al archivo principal de **` zsh `** y sus configuraciones acceder [AQUI](shells/zsh/zshrc.md)
