---
typora-root-url: ./
---


![](/Geant4/images/b2b_0000.png)

# Instalación completa de Geant4 y ROOT

En este repositorio se muestra el proceso detallado para realizar una instalación completa e integrada entre Geant4 y ROOT. Se dirige a usuarios noveles y medios. El proceso funciona para las siguientes distribuciones basadas en *apt* o en *pacman*.

* **Debian (10), Debian (10) Linux Mint (18.2)**

  Estas distribuciones hacen uso de `apt` para gestionar los paquetes. Para instalar un paquete nuevo el comando es el siguiente: 

  ```bash
  $ sudo apt install nombre_paquete
  ```

* **Manjaro (18.0.4)**

  Estas distribuciones hacen uso de `pacman` para gestionar los paquetes. Para instalar un paquete nuevo el comando es el siguiente:

  ```bash
  $ sudo pacman -S nombre_paquete
  ```

  

El esquema final de la instalación será el siguiente:


![](/src/dir_general.png)



## Geant4 10.05.p01
---

Geant4 es un "toolkit" (caja de herramientas) para la simulación del paso de partículas a través de la materia. Su proceso de instalación no es trivial, fácilmente puede disuadir a usuarios poco experimentados, pero constituye un paso importante para ingresar a mundo de la simulación. El proceso de instalación que usaremos será el siguiente:

* Preparación del sistema
* Instalación para apt systems y pacman systems
* Instalación para pacman systems

### Preparación del sistema

1. ACTUALIZAR la distribución de Linux a la versión más reciente:

   ```bash
   $ sudo apt update
   ```

   ```bash
   $ sudo apt upgrade
   ```

2. INSTALAR DEPENDENCIAS

   Los paquetes han sido revisados con la base de paquetes de [Ubuntu](https://packages.ubuntu.com/).

   **Librerías necesarias para Geant4 y ROOT:**

   ```bash
   $ sudo apt install libxerces-c-dev mesa-utils mesa-utils-extra mesa-common-dev libfreetype6 libfreetype6-dev libxmu-dev qt4-default libqt4-opengl libqt4-opengl-dev qt5-default libqt5opengl5 libqt5opengl5-dev
   ```

   ```bash
   $ sudo apt install cmake cmake-qt-gui g++ gcc gfortran binutils libx11-dev libxpm-dev libxft-dev libxext-dev libpng-dev libpng++-dev libjpeg-dev
   ```

   Librerías importantes (opcionales):

   ```bash
   $ sudo apt install git libssl-dev libpcre3-dev libftgl-dev libmysqlclient-dev libfftw3-dev libcfitsio-dev graphviz-dev libavahi-compat-libdnssd-dev libldap2-dev python-dev libxml2-dev libkrb5-dev libgsl23 libgsl-dev
   ```

### Instalación Geant4

* [**Distribuciones: Debian/Ubuntu/Mint**](/Geant4/install_geant4.md)

* **Distribuciones Arch/Manjaro**

  El proceso de instalación de geant4 en distribuciones *Arch* es esencialmente la misma que las basadas en *Debian*. La única diferencia consiste en buscar los paquetes para `pacman` (generalmente estas distros ya traen la mayoría de esos paquetes instalados). Para realizar la búsqueda de los paquetes se recomienda utilizar el *gestor de software* propio de esas distribuciones **pamac** u **octopi** que hacen una gestión excelente. Los comandos para fijar variables de entorno y para ejecutar los programas es exactamente igual. Nota.- (pacman = terminal, pamac = interfaz gráfica de pacman).

  Los paquetes también se puede buscar directamente en página oficial de Arch

  * https://www.archlinux.org/packages/

---
## ROOT 6.18.00
---

| Logo ROOT               | Imagen .demo de ROOT  |
| ----------------------- | --------------------- |
| ![](/src/logo_root.png) | ![](/src/root-gh.png) |

### Preparación del sistema

En general, una vez instalado Geant4, la instalación de ROOT es relativamente sencilla. En caso de solamente requerir ROOT, el proceso de resume a continuación:

* Actualizar el sistema

* Instalar dependencias

  ```bash
  $ sudo apt install git cmake cmake-qt-gui g++ gcc binutils libx11-dev libxpm-dev libxft-dev libxext-dev libpng-dev libpng++-dev libjpeg-dev gfortran
  ```

* Proceder a la instalación del software eligiendo una de las dos formas:

  * Desde el código fuente
  * Desde paquete pre-compilado

***

### [Instalación desde el código fuente](/ROOT/install_ROOT.md) 

La instalación de ROOT desde el código fuente es tradicionalmente la mejor opción. 

**Ventajas e inconvenientes de compilar:**

+ El software aprovechará toda la potencia que brinde nuestro ordenador. 
+ Es especialmente útil cuando se cuenta con un ordenador potente en el que se desee aprovechar todos los recursos disponibles.
+ Útil cuando se quiere optimizar el tiempo de cálculo de un ordenador modesto.
+ Es un proceso largo y algo tedioso.



### [Instalación pre-compilada](/ROOT/binary_ROOT.md)

La instalación pre-compilada consiste en una instalación rápida. En esta modalidad, el software ha sido compilado en otro ordenador bajo ciertas condiciones (dependencias) que tienen que cumplirse en el ordenador de destino para que se ejecute.

**Ventajas e inconvenientes de usar pre-compilado:**

* Es es una instalación relativamente rápida.
* Es la mejor opción para usuarios nóveles porque no requiere compilar desde el código fuente.
* No aprovecha todos los recursos de nuestro ordenador. Solo se nota al realizar análisis de datos de gran complejidad.



---

# Fuentes y Recursos:

* [Geant 4 (Download page and more)](http://geant4.web.cern.ch/)
* [ROOT Documentation](https://root.cern.ch/documentation)

