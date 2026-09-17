# Compresión y descompresión en ensamblador 88110

## Descripción
Proyecto desarrollado en **ensamblador para el Motorola 88110** que implementa un sistema de compresión y descompresión de cadenas de texto sin pérdidas.

El programa busca secuencias repetidas dentro del texto y las sustituye por referencias a apariciones anteriores, reduciendo así el tamaño de los datos almacenados. Posteriormente, el texto comprimido puede ser reconstruido mediante el proceso de descompresión.

## Arquitectura

### Rutinas

La implementación está dividida en diferentes rutinas que se encargan de las distintas partes del proceso:

`LongCad` — Obtiene la longitud de una cadena.

`BuscaCar` — Busca un carácter dentro de una cadena.

`CoincidenCad` — Calcula la longitud de una coincidencia entre cadenas.

`BuscaMax` — Busca la coincidencia más larga.

`PoneBitA1` — Activa un bit determinado.

`Comprime` — Realiza la compresión del texto.

`LeeBit` — Lee un bit determinado.

`Descomprime` — Reconstruye el texto original.

`Verifica` — Comprueba que la descompresión reproduce correctamente el texto original.

### Funcionamiento

Los procesos principales del proyecto son:

#### Compresión:

1. Se recorre el texto original y se obtiene su longitud con `LongCad`.

2. Se buscan secuencias repetidas dentro del texto con `BuscaCar` y `CoincidenCad`.

3. Se determina la coincidencia más larga con `BuscaMax`.

4. Las secuencias repetidas se sustituyen por referencias a apariciones anteriores.

5. Los caracteres que no se pueden comprimir se mantienen directamente.

6. Se activan los bits correspondientes en el mapa de bits con `PoneBitA1`. 

7. `Comprime` coordina todo el proceso y genera el texto comprimido con:
   - Cabecera.
   - Mapa de bits.
   - Caracteres y referencias.

#### Descompresión:

1. `Descomprime` lee la información del texto comprimido.

2. Se recorre el mapa de bits leyendo cada bit con `LeeBit`.

3. Los caracteres se copian directamente.

4. Las referencias se utilizan para reconstruir las secuencias repetidas.

5. Se obtiene de nuevo el texto original.

#### Verificación:

1. `Verifica` compara el texto original con el texto obtenido después de la descompresión para comprobar que el proceso es sin pérdidas.

### Tecnologías

Lenguaje ensamblador en arquitectura **Motorola 88110**

## Estructura del proyecto

```plaintext
.
├── CDV25.ens         # Código fuente del proyecto en ensamblador.
├── INSTRUCTIONS.md   # Instrucciones de instalación y ejecución del proyecto
└── README.md         # Descripción del proyecto
```

## Instalación y ejecución

Ver [INSTRUCTIONS.md](INSTRUCTIONS.md)
