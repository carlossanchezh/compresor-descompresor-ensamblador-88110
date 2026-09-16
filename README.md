# Compresión y descompresión en ensamblador 88110

## Descripción
Proyecto desarrollado en **ensamblador para el Motorola 88110** que implementa un sistema de compresión y descompresión de cadenas de texto sin pérdidas.

El programa busca secuencias repetidas dentro del texto y las sustituye por referencias a apariciones anteriores, reduciendo así el tamaño de los datos almacenados. Posteriormente, el texto comprimido puede ser reconstruido mediante el proceso de descompresión.

## Arquitectura

### Rutinas

La implementación está dividida en diferentes rutinas que se encargan de las distintas partes del proceso:

1. `LongCad` — Obtiene la longitud de una cadena.
2. `BuscaCar` — Busca un carácter dentro de una cadena.
3. `CoincidenCad` — Calcula la longitud de una coincidencia entre cadenas.
4. `BuscaMax` — Busca la coincidencia más larga.
5. `PoneBitA1` — Activa un bit determinado.
6. `Comprime` — Realiza la compresión del texto.
7. `LeeBit` — Lee un bit determinado.
8. `Descomprime` — Reconstruye el texto original.
9. `Verifica` — Comprueba que la descompresión reproduce correctamente el texto original.

### Funcionamiento

Los procesos principales del proyecto son:

#### Compresión:

1. Se recorre el texto original.
2. Se buscan secuencias repetidas.
3. Las secuencias repetidas se sustituyen por referencias.
4. Los caracteres que no se pueden comprimir se mantienen directamente.
5. Se genera el texto comprimido con:
   - Cabecera.
   - Mapa de bits.
   - Caracteres y referencias.

#### Descompresión:

1. Se lee la información del texto comprimido.
2. Se recorre el mapa de bits.
3. Los caracteres se copian directamente.
4. Las referencias se utilizan para reconstruir las secuencias repetidas.
5. Se obtiene de nuevo el texto original.

#### Verificación:

1. Se compara el texto original con el texto obtenido después de la descompresión para comprobar que el proceso es **sin pérdidas**.

### Tecnologías

Lenguaje ensamblador en arquitectura **Motorola 88110**

## Estructura del proyecto

```plaintext
.
├── CDV25.ens  # Código fuente del proyecto en ensamblador.
├── INSTRUCTIONS.md # Instrucciones de instalación y ejecución del proyecto
└── README.md # Descripción del proyecto
```

## Instalación y ejecución

Ver [INSTRUCTIONS.md](INSTRUCTIONS.md)
