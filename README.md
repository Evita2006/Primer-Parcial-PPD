# Procesador de Imágenes Satelitales

El sistema gestiona la entrada de datos de satélites y su procesamiento mediante hilos independientes.

## Cómo funciona
1. Receptor (Hilo 1): Guarda las imágenes según llegan en una Cola.
2. Analista (Hilo 2): Saca las imágenes de la cola una por una para procesarlas.
3. La Cola (FIFO): Asegura que no se pierda ninguna imagen y que se procesen en orden de llegada, sirviendo como un "colchón" cuando el satélite envía muchas imágenes rápido.

## Ejecución
Para arrancar el sistema, usa el siguiente comando en tu terminal:
```bash
python procesamiento.py
