# Instalación de Geant4-10.05.p01

## Instalación desde el código fuente

![](/home/jonasdx/MEGA/TFM_Jonas/geant4-and-root/Geant4/images/dir_geant4.png)

1. Descargar el código fuente desde la página oficial de **Geant4 10.05.p01**

   [Gnu or Linux tar format, compressed using gzip](http://geant4.web.cern.ch/support/download)

2. Descargar todos los paquetes adicionales de la sección: ***DATA FILES ( )***. Son necesarios para ejecutar los ejemplos de simulación que trae Geant4.

   Son en total 12 archivos: G4NDL4.5, G4EMLOW7.7, G4PhotonEvaporation5.3, etc.

3. Descomprimir el código fuente y renombrar la carpeta de la siguiente forma:

   **geant4.10.05.p01** ---por---> **g4_source**

4. Prestar atención al esquema de instalación.

5. Mover la carpeta **g4_source** a la ruta de instalación: ***/home/USUARIO/MIENTORNO/Geant4-10.05/***

6. Descomprimir todos los archivos adicionales dentro de una carpeta denominada: **data**

7. Mover la carpeta **data** a la ruta de instalación: ***/home/USUARIO/MIENTORNO/Geant4-10.05/***

8. Dentro de la ruta de instalación crear dos directorios adicionales:

   **geant_build** y **geant_install**

9. En este punto debemos tener el siguiente lo siguiente

   ```bash
   $ ls
   ```

   ```bash
   output:
   data  g4_build  g4_install  g4_source  geant4.10.05.p01.tar.gz
   ```

10. a

11. b

12. c



## Configurar entorno de variables



