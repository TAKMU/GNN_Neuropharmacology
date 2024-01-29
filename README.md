# GNN_Neuropharmacology
## Requisitos
- Conda
- Python= 3.11
- PyTorch = 2.1.2
- PyTorch_Geometric (pyg) = 2.4.0

(paquetes adicionales que necesitan instalarse por cuenta propia, las instrucciones se encuentran en Instalación)

- torch_scatter 
- torch_sparse 
- torch_cluster 
- torch_spline_conv 

## Instalación 
El proyecto está utilizando un entorno virtual conda. Favor de instalar conda si no lo tiene instalado, [página de instalación](https://conda.io/projects/conda/en/latest/index.html). 

El entorno virtual se puede crear con el siguiente comando:

>conda env create -f environment.yml

Para activar el entorno virtual, necesita utilizar el siguiente comando (*Nota: en algunos editores de texto como VS Code, no se activan directamente, se necesita elegir el intérprete*) :

>conda activate gnn_project_1

>conda env list</br>
gnn_project_1      *  C:\Users\myuser\anaconda3\envs\gnn_project_test

**Importante: Se necesita instalar paquetes adicionales**

Para instalar los paquetes adicionales, favor de revisar la versión de Pytorch y cuda. 

>(1) python -c "import torch; print(torch.__version__)"

>(2) python -c "import torch; print(torch.version.cuda)"

Se instalan los paquetes restantes con el siguiente comando:

>pip install pyg_lib torch_scatter torch_sparse torch_cluster torch_spline_conv -f https://data.pyg.org/whl/torch-${TORCH}+${CUDA}.html

En donde ${TORCH} es igual a la versión de torch (1), y ${CUDA} es igual a la versión de cuda (2).

**Importante: Si recibe error de que no puede instalar pyg_lib, favor de eliminar el paquete del comando.**

>pip install torch_scatter torch_sparse torch_cluster torch_spline_conv -f https://data.pyg.org/whl/torch-${TORCH}+${CUDA}.html

Ejemplo (PyTorch==2.1.0, CUDA = cpu)

>pip install torch_scatter torch_sparse torch_cluster torch_spline_conv -f https://data.pyg.org/whl/torch-$2.1.0+cpu.html

