# cdaa-customer-churn

Tarea de asignatura de Ciencia de datos y Aprendizaje automático basada en la competición en Kaggle (Retención de clientes para una entidad financiera)[https://www.kaggle.com/competitions/retencion-de-clientes-de-una-entidad-financiera]

```
La pestaña Data encontraremos los siguientes ficheros: train.csv, test.csv y sample_submission.csv. El conjunto de datos de entrenamiento se encuentra en train.csv y consta de 8000 instancias. Por su parte, el conjunto de datos de prueba es test.csv, está formado por 2000 instancias y se utilizará para realizar la predicción. 
```
# How to

## Directorios kaggle
Para tener portabilidad entre el entorno de trabajo y kaggle creamos los siguientes directorios de trabajo

```bash
sudo mkdir -p /kaggle/input/retencion-de-clientes-de-una-entidad-financiera/          #ficheros de entrada
sudo mkdir -p /kaggle/working/              #ficheros de salida
sudo chown tu_usuario:tu_grupo -R /kaggle   #propietario de los directorios/ficheros
```

## Instalación del entorno en linux

Instalar conda usando Miniforge (que incluye Mamba).

```bash
wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh"

Ejecutar el script de instalación
bash Miniforge3-Linux-x86_64.sh

# 3. Sigue las instrucciones en pantalla:
#    - Presiona Enter para leer la licencia.
#    - Escribe 'yes' para aceptar.
#    - Presiona Enter para confirmar la ruta de instalación.
#    - IMPORTANTE: Escribe 'yes' cuando pregunte si deseas inicializar Miniforge3.

# cierra y vuelve a abrir la termina o ejecuta lo siguiente
source ~/.bashrc
```
Crear un entorno de mamba o conda

```
mamba create -n pcd_env python=3.12 -y
mamba activate pcd_env
```


Instalar el stack de DS y herramientas de desarrollo
```

mamba install -c conda-forge \
    jupyter \
    ipykernel \
    pandas \
    numpy \
    matplotlib \
    seaborn \
    scikit-learn \
    xgboost \
    imbalanced-learn \
    category_encoders -y
```