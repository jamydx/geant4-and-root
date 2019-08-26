# Instalación de ROOT 6.18

### Detalles de la instalación de ROOT 6.18

Este proceso de instalación esta dirigido a usuario poco experimentados por lo tanto hace uso en la mayoría de las veces el *gestor de archivos*. En general, para instalar este software solo necesitamos el código fuente y una carpeta ***build*** donde compilar. Se recomienda realizar una instalación ordenada como se muestra en el esquema adjunto (todos los directorios son carpetas).

----



![](/path6565.png)

### Pasos a seguir:

1. Descargar los binarios desde la página oficial de [ROOT](https://root.cern.ch/downloading-root) . Seleccionar la última versión estable. 

   [root_v6.18.00.source.tar.gz](https://root.cern/download/root_v6.18.00.source.tar.gz), (158 MB)

2. Mover el archivo descargado a nuestro directorio de instalacion ***root-6.18***:

3. Descomprimir el archivo comprimido (.tar.gz). 

   Revisar que se haya creado la carpeta: ***root-6.18.00***

4. Crear el directorio *root-build*.

   Comprobar que todo este de acuerdo al esquema adjunto.

5. Abrir una terminal y cambiar al directorio actual: *root-build*

   ```bash
   $ cd /home/USUARIO/Documents/ENTORNO/root-6.18/root-build/
   ```

6. Ejecutar `cmake`

   ```bash
   $ camke ../root-6.18.00/
   ```

7. Compilar root

   Sino observas ningun problema, todo está listo para la compilación. Aqui `j4` significa que vamos a compilar usando 4 nucleos del procesador,  depende de la potencia de tu ordenador.  Mientras más núcleos físicos poseas menos tiempo tomará el proceso y viceversa. Con mi ordenador y usando 4 núcleos el proceso tardó: 1h y 30 min.

   ```bash
   $ make -j4
   ```

8. Fijar las varibales de entorno
   ```bash
   $ source /bin/thisroot.sh
   ```

9. Ya tenemos instalado ROOT

   ```bash
   $ root
   ```




## ROOT de forma persistente `(source)`

Con el proceso anterior ya se tiene correctamente instalado *ROOT*, sin embargo, el paso 8 se tiene que realizar cada vez que se cierre la terminal, por lo que es mejor fijar *ROOT* de forma persistente. El proceso es el siguiente:

   - Abrir el directorio home: */home/*usuario/

   - Presionar `Crtl + H` para ver los archivos ocultos.

   - Localizar el archivo `.bashrc`

   - Abrir `.bashrc` con un editor de texto, ir al final del todo y pegar lo siguiente:

     (Cambia USUARIO por el tuyo)

     ```bash
     # Entorno de Geant4 y ROOT
     source /home/USUARIO/Documents/Geant4/root-6.18/root-build/bin/thisroot.sh
     ```

- Guardamos, salimos y presionar nuevamente `Crtl + H` para regresar todo a la normalidad.

* Ahora podemos ejecutar *root* desde cualquier parte del ordenador

   ```bash
   $ root
   ```



## Adicional

### Vincular *ROOT* con *Geant4*. 

Esto es especialmente útil cuando se requiere que la simulación llame a ROOT para llenar un histograma directamente, etc.  

El procedimiento es el siguiente:

Movernos a la ruta de instalación de root y crear un archivo nuevo llamado: `root.sh`, así:

   ```bash
   $ cd /home/user/Documents/ENTORNO/root-6.18/
   $ touch root.sh
   ```

10. Abrir el archivo que hemos creado y pegar dentro lo siguiente:

    ```bash
    # Mensaje para mostrar en la terminal
    echo Root en Geant4 listo!
    
    # Para usar ROOT con Geant4 en algunas aplicaciones
    export G4ROOT_USE=1
    ```

  

El resultado final es el siguiente:

![](/root-final.png)

Cuando root ha sido compilado desde el código fuente se puede ver el mensaje:

```bash
Built for linuxx8664gcc on Aug 25 2019, The ROOT Team
```

FIN
