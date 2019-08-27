
![](/Geant4/images/b2b_0000.png)

# Instalación completa de Geant4 y ROOT

En este repositorio se muestra el proceso detallado para realizar una instalación completa e integrada entre Geant4 y ROOT. Se dirige a usuarios noveles y medios. El proceso sirve para la siguiente lista de distribuciones:


| Apt (base)                                                 | Pacman (base)    |
| ---------------------------------------------------------- | :--------------- |
| Debian (stable)<br />Ubuntu (18.04)<br />Linux Mint (18.2) | Manjaro (18.0.4) |

Esquema general de los directorios de instalación:

![](/src/dir_general.png)


## Geant4.10.05.p01

#### Preparación del sistema

1. ACTUALIZAR la distribución de Linux a la versión más reciente:

   ```bash
   $ sudo apt update
   ```

   ```bash
   $ sudo apt upgrade
   ```

2. INSTALAR DEPENDENCIAS

   Los paquetes han sido revisados con la base de paquetes de [Ubuntu](https://packages.ubuntu.com/).

   **Librerías necesarias: Geant4 y ROOT:**

   ```bash
   $ sudo apt install libxerces-c-dev mesa-utils mesa-utils-extra mesa-common-dev libfreetype6 libfreetype6-dev qt4-default libqt4-opengl libqt4-opengl-dev libxmu-dev qt5-default
   ```

   ```bash
   $ sudo apt install git cmake cmake-qt-gui g++ gcc binutils libx11-dev libxpm-dev libxft-dev libxext-dev libpng-dev libpng++-dev libjpeg-dev gfortran
   ```

   Librerías importantes (opcionales):

   ```bash
   $ sudo apt install libssl-dev libpcre3-dev libftgl-dev libmysqlclient-dev libfftw3-dev libcfitsio-dev graphviz-dev libavahi-compat-libdnssd-dev libldap2-dev python-dev libxml2-dev libkrb5-dev libgsl23 libgsl-dev
   ```

---

### Instalación para distribuciones: Debian/Ubuntu/Mint

Estas distribuciones hacen uso de `apt` para gestionar los paquetes: 

```bash
$ sudo apt install paquete
```

Las instrucciónes para la instalación completa de Geant4 se muestro a continuación

* [Geant4 para Debian/Ubuntu/Mint](/Geant4/install_geant4.md)

### Instalación para distribuciones en Arch/Manjaro

Estas distribuciones hacen uso de `pacman` para gestionar los paquetes:

```bash
$ sudo pacman -S paquete
```

La instalación en distribuciones Arch es la misma que las basadas en Debían. La única diferencia consiste en buscar los paquetes en su versión Arch (generalmente ya traen muchos paquetes instalado), los demás comandos son exactamente iguales. Para realizar buscar los paquetes se recomienda utilizar el *gestor de software* propio de esas distribuciones `pamac` u `octopi` que hacen una gestion excelente.




## ROOT 6.18.00

| Logo ROOT               | Imagen demo de ROOT   |
| ----------------------- | --------------------- |
| ![](/src/logo_root.png) | ![](/src/root-gh.png) |

#### Preparación del sistema

En general, una vez instalado Geant4, la instalación de ROOT es relativamente sencilla. En caso de solo requerir ROOT no hay problema, el proceso de resume a continuación:

* Actualizar el sistema

* Instalar depencias

  ```bash
  $ sudo apt install git cmake cmake-qt-gui g++ gcc binutils libx11-dev libxpm-dev libxft-dev libxext-dev libpng-dev libpng++-dev libjpeg-dev gfortran
  ```

* Proceder a la instalación del software elgiendo una de las dos formas:

  * Desde el código fuente
  * Desde paquete pre-compilado

---

#### Instalación desde el código fuente

La instalación de ROOT desde el código fuente es la mejor opción. 

**Ventajas e inconvenientes de compilar:**

+ El software aprovechará toda la potencia que brinde nuestro ordenador. 
+ Es especialmente útil cuando se cuenta con un ordenador potente en el que se desee aprovechar todos los recursos disponibles.
+ Útil cuando se quiere optimizar el tiempo de cálculo de un ordenador modesto.
+ Es un proceso largo y algo tedioso.

**Instrucciones para realizar esta instalación se muestra a detalle aquí:** 

* [Instalar ROOT desde código fuente](/ROOT/install_ROOT.md)

---

#### Instalación pre-compilada

La instalación pre-compilada consiste en una instalación rápida. El software ha sido compilado en otro ordenador bajo ciertas condiciones (dependencias) que tienen que cumplirse en el ordenador de destino para que se ejecute.

**Ventajas e inconvenientes de usar pre-compilado:**

* Es es una instalación relativamente rápida.
* Es la mejor opción para usuarios nóveles porque no requiere compilar desde el código fuente.
* No aprovecha todos los recursos de nuestro ordenador. Solo se nota al realizar análisis de datos de gran complejidad.

**Instrucciones para realizar esta instalación se muestran aquí:** 

* [Instalar ROOT desde pre-compilado](/ROOT/binary_ROOT.md)



---

## Fuentes y Recursos:

* [Geant 4 (Download page and more)](http://geant4.web.cern.ch/)
* [ROOT Documentation](https://root.cern.ch/documentation)

