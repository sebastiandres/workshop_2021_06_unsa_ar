# HELP

## Crear el ambiente
conda create -n workshop_unsa

# Instalar librerías
Desde requirements:
source activate workshop_unsa
conda install --file requirements.txt

Uno a uno:
pip install rise
pip install pandas
(rise instala jupyter notebook & all, pandas instala numpy y matplotlib)

## Generar un pdf con las slides
Ejecutar
jupyter nbconvert --to slides workshop_unsa.ipynb --post serve

Abrir
http://127.0.0.1:8000/workshop_unsa.slides.html

Agregar "?print-pdf" al enlace
http://127.0.0.1:8000/workshop_unsa.slides.html?print-pdf

Puedes hacer los 2 al mismo tiempo, y ahora guardas como pdf (Ctrl/Cmmd+P):
jupyter nbconvert --to slides workshop_unsa.ipynb --post serve; open http://127.0.0.1:8000/workshop_unsa.slides.html?print-pdf

## Borrar el ambiente
conda deactivate
conda env remove -n workshop_unsa

## Mostrar todos los ambientes
conda env list

## Actualizar index.html
Reemplazar REPOSITORY por el nombre del repositorio.
Recordar activar github pages en la rama principal y directorio principal.
