# Comandos básicos de Linux

Estos son los comandos más básicos para inciar en Linux. Para probarlos inicia una *Terminal* y escríbelos en ella.

1. Listar archivos de un directorio: `ls`
2. Conocer en que directorio estamos actualmente: `pwd`

## Comandos para administar directorios y archivos

En general para este proceso de intalación preferimemos utilizar el *gestor de archivos* sobre los comandos de terminal, sin embargo,  eventualmente tendremos que utilizarlos.

1. Crear un Nuevo Directorio o carpeta: `mkdir nueva_carpeta`
2. Copiar  un archivo o un directorio: `cp FUENTE DIRECTORIO`
3. Mover un archivo o un directorio: `mv FUENTE DIRECTORIO`

## Comandos para utilizar el superusuario

Cambiar a super usuario nos permite realizar acciones que normalmente no son permitidas para las cuentas de usuario normales. La contraseña por lo general es la misma que con la que se inicia sesión al encender el ordenador.

1. Ejecutar comando como super usuario

   ```bash
   $ sudo comando_a_ejecutar
   [sudo] password for your_user: 
   $
   ```

2. Cambiar a super usuario. Se recomienda discreción al cambiar a modo superusuario porque tenemos luz verde para borrar archivos, mover, etc. que podría romper el sistema sino se sabe lo que se hace. Notese que `$`, cambia a `#`
   ```bash
   $ sudo su
   [sudo] password for your_user: 
   #
   ```
