# Terminal de Linux

## Comandos básicos

Estos son los comandos básicos para iniciar en Linux. Para probarlos inicia una *Terminal*.

1. Listar archivos de un directorio 

   ```bash
   $ ls
   ```

2. Conocer en que directorio actual

   ```bash
   $ pwd
   ```

   

## Comandos para administrar directorios y archivos

En general para este proceso de instalación se prefiere utilizar el *gestor de archivos* sobre los comandos de terminal, sin embargo,  eventualmente tendremos que utilizarlos.

1. Crear un Nuevo Directorio o carpeta: `mkdir nueva_carpeta`
2. Copiar  un archivo o un directorio: `cp FUENTE DIRECTORIO`
3. Mover un archivo o un directorio: `mv FUENTE DIRECTORIO`

## Comandos para utilizar el superusuario

Cambiar a superusuario nos permite realizar acciones que normalmente no son permitidas para las cuentas de usuario normales. La contraseña por lo general es la misma que con la que se inicia sesión al encender el ordenador.

1. Ejecutar comando como superusuario

   ```bash
   $ sudo comando_a_ejecutar
   --> [sudo] password for your_user: 
   ```

   ```bash
   output:
   $
   ```

   

2. Cambiar a **superusuario** (root) no confundir con el programa que vamos a instalar. Se recomienda discreción al cambiar a modo superusuario porque tenemos luz verde para borrar archivos, mover, etc. que podría romper el sistema sino se sabe lo que se hace. Notese que `$`, cambia a `#`

   ```bash
   $ sudo su
   --> [sudo] password for your_user: 
   ```

   ```bash
   output:
   # 
   ```

   
