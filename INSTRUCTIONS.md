# Instrucciones de Instalación y Ejecución

Este documento describe los requisitos, la instalación y la ejecución del proyecto **Compresor/Descompresor en ensamblador para el Motorola 88110**.

## Requisitos

- Un **emulador** compatible con el Motorola 88110.

- Un **ensamblador** compatible con el Motorola 88110.

## Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/carlossanchezh/compresor-descompresor-ensamblador-88110.git
```

### 2. Preparar el emulador y el ensamblador

Este repositorio no incluye el emulador ni el ensamblador. 

Debes disponer de una herramienta compatible con el MC88110 y seguir las instrucciones de instalación y uso del ensamblador/emulador que hayas elegido para:

- Ensamblar el fichero `CDV25.ens`.

- Ejecutar el binario resultante en el emulador.

## Ejecución

### 1. Ensamblado

Usa tu ensamblador compatible con el MC88110 para traducir `CDV25.ens` a un binario ejecutable.

### 2. Ejecución en el emulador

Carga el binario generado en tu emulador compatible con el MC88110 y ejecútalo siguiendo las instrucciones de dicha herramienta.