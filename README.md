# bluetab_OCR
 La siguiente prueba tiene como objetivo evaluar el manejo de herramientas OCR para la extracción de datos.
 Además de la lectura y reconstrucción de archivos.

## Estructura general
Se usará streamlit como una interfaz práctica para el usuario, además del servicio de despliegue.
La estructura general del proyecto (que se espera conservar) hasta la versión V.1.1.0 es:
```
prueba_OCR/
├── datos/
|   └── instrucciones.txt
├── hocr/
|   ├── 1C_5.hocr
|   ├── 1E_1.hocr
|   └── 3T_4.hocr
├── recursos/
|   ├── 1C.pdf
|   ├── 1E.pdf
|   ├── 3T.pdf
|   ├── Prueba tecnica para desarrollador IA_ revisado.pdf
|   └── notas.txt
├── main.py
├── requirements.txt
└── README.md
```

### V.1.0.0
Interfaz inicial y despliegue en el servicio de nube.

### V.1.1.0
Se estructura el proyecto en subcarpetas con recursos de apoyo como las vistas previas de PDF, las instrucciones revisadas, etc., además de los archivos .hocr y algunos datos como archivos de texto grandes que se leen en la interfaz pero no están incrustados directamente en el código y un archivo de notas donde se ponen notas mentales yb funciones pasadas como referencia.

### V.1.2.2
Los PDF de referencia ahora se despliegan en una vista previa para el usuario y una tabla con los datos extraídos de cada documento, además de que la función que encuentra las líneas lo guarda en DataFrames de cada documento.

### V.1.2.3
No se logró con exito total el usar las etiquetas de ocr_carea como haders de los DataFrames para poder separar las líneas en una estructura distinta.
En esta versión la lectura queda a medias por un error en los bucles que forman bloques con las etiquetas predeterminadas.

### V.1.3.2
Se hizo un cambio en la función de la lectura de los archivos .hocr que ahora busca las etiquetas carea para formar bloques en donde introduce las etiquetas de ese bloque, procurando formar una tabla estructurada que recupere los datos y los reconstruya.
(La tabla no reconstruye el documento, pero presenta la información con uns estructura nueva).