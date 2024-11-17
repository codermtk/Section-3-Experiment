# Autoencoder-Based Image Clustering and Visualization

This repository contains the code necessary to train the autoencoder used by AM in:
*"Logic Is Not Universal: Dismantling the Illusion of Reason ’*.
It learns latent representations of images and includes clustering with DBSCAN and visualisation using UMAP.

Este repositorio contiene el código necesario para entrenar el autoencoder usado por AM en:
*"La Lógica No es Universal: Desmantelando la Ilusión de la Razón"*.
Aprende representaciones latentes de imágenes e incluye clustering con DBSCAN y visualización mediante UMAP.

## Languages / Idiomas

- [English](#instructions-in-english)
- [Español](#instrucciones-en-español)

---

## Instructions in English

### Requirements
1. Install Python 3.8 or higher.
2. Install the required dependencies from `requirements.txt`:
   Example: pip install -r requirements.txt
3. Dataset Access
   Download the dataset from the following link and place it in the data folder:
   https://huggingface.co/datasets/gabrielmfr/section3

Example directory structure:

/data
  ├── Screenshot_1.png
  ├── Screenshot_2.png
  └── Screenshot_3.png
  
### Usage
1. Dataset Preparation
   - Place the downloaded dataset in the data folder.
   - Update the img_dir variable in the notebook with the path to your image directory:
   Example: img_dir = "data"
2. Train the autoencoder
   - Open the notebook and run the cells to train the autoencoder on your dataset.
3. Configuration options:
   - Batch size: Adjust in the dataloader definition.
   - Latent dimension: Update the latent_dim variable in the autoencoder class.
3. Cluster latent representations
   The notebook will:
   1. Extract latent representations of images.
   2. Perform clustering using DBSCAN.
   3. Visualize the clusters in 2D space using UMAP.
4. Visualize new images
   - Use the project_and_plot_new_image() function to project a new image into the UMAP space:
   Example: new_image_path = "path_to_new_image.png"
            project_and_plot_new_image(new_image_path)

## Instrucciones en Español

### Requisitos
1. Instalar Python 3.8 o superior.
2. Instale las dependencias requeridas de `requirements.txt`:
   Ejemplo: pip install -r requirements.txt
3. Acceso al conjunto de datos
   Descargue el conjunto de datos desde el siguiente enlace y colóquelo en la carpeta de datos:
   https://huggingface.co/datasets/gabrielmfr/section3

Ejemplo de estructura de directorios:

/data
  ├── Captura de pantalla_1.png
  ├── Captura de pantalla_2.png
  └── Captura de pantalla_3.png

### Uso
1. Preparación del conjunto de datos
   - Coloque el conjunto de datos descargado en la carpeta de datos.
   - Actualice la variable img_dir en el bloc de notas con la ruta a su directorio de imágenes:
   Ejemplo: img_dir = «data»
2. Entrene el autoencoder
   - Abra el cuaderno y ejecute las celdas para entrenar el autoencoder en su conjunto de datos.
3. Opciones de configuración:
   - Tamaño del lote: Ajustar en la definición del dataloader.
   - Dimensión latente: Actualizar la variable latent_dim en la clase autoencoder.
3. Agrupar representaciones latentes
   El cuaderno hará:
   1. Extraer representaciones latentes de las imágenes.
   2. Realizar clustering utilizando DBSCAN.
   3. Visualizar los clusters en el espacio 2D utilizando UMAP.
4. Visualizar nuevas imágenes
   - Utilice la función project_and_plot_new_image() para proyectar una nueva imagen en el espacio UMAP:
   Ejemplo: ruta_nueva_imagen = «ruta_a_nueva_imagen.png»
            proyectar_y_trazar_nueva_imagen(ruta_nueva_imagen)
