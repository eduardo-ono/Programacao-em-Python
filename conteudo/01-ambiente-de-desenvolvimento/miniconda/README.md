
<h1 align="center">
Miniconda
</h1>

<h4 align="center">Prof. Eduardo Ono</h4>

<br>

## Instalação do Miniconda + Pacotes (Windows)

* Overview

    * A instalação do Miniconda já inclui o Python e o gerenciador de pacotes Pip.

    * Python

      https://www.youtube.com/watch?v=XCvgyvBFjyM

* Download

    * https://docs.conda.io/en/latest/miniconda.html

* Instalação do Miniconda

    * Instalar com as opções "default".

* Atualização do Miniconda

```bash
conda update conda
```

<br>

## Configuração do Miniconda

* Para tornar "default" o repositório conda-forge, abrir o terminal "Anaconda Prompt" (criado na instalação do Miniconda) e digitar:

```cmd
conda config --add channels conda-forge
conda config --set channel_priority strict
```

## Instalação do JupyterLab

* Abrir o terminal "Anaconda Prompt" e, no ambiente `base`, digitar:

```cmd
conda install jupyterlab
```

* Caso o repositório "default" não tenha sido configurado, digitar:

```cmd
conda install -c conda-forge jupyterlab
```

<br>

## Instalação e Configuração do Miniconda (Linux)

### Vídeos de Apoio

| Thumb | Descrição |
| :-: | --- |
| [![img](https://img.youtube.com/vi/Tk-B6Nm8qOY/default.jpg)](https://www.youtube.com/watch?v=Tk-B6Nm8qOY) | <sup>[josé henrique padovani]</sup><br>[__4 [linux/ubuntu] - Instalação do miniconda, Python e Jupyter__](https://www.youtube.com/watch?v=Tk-B6Nm8qOY)<br><sub>(14:14, YouTube, Out/2021)</sub>

<br>

## Gerenciamento de Ambientes Virtuais com o Conda

* Exibir informação sobre o ambiente

```sh
conda info
```

* Listar todos os ambientes configurados

```sh
conda env lista
```

* Criar um ambiente (abreviado aqui como "env", de _environment_):

```sh
conda create -n <env_name>
# ou
conda create --name <env_name>
```

* Exemplos:

```sh
conda create -n abacaxi
conda create --name abacaxi
```

* Criar um novo ambiente com alguns pacotes:

```sh
conda create -n <env_name> pandas numpy matplotlib scikit-learn
```

* Ativar um ambiente

Para que um ambiente virtual possa ser utilizado, o mesmo deve ser ativado:

```sh
conda activate <env_name>
```

* Desativar o ambiente atual

```sh
conda deactivate
```

* Desativar um ambiente

```sh
conda deactivate <env_name>
```

* Desativar o ambiente (base)

```sh
conda config --set auto_activate_base false
```

* Ativar o ambiente (base)

```sh
conda config --set auto_activate_base true
```

* Remover um ambiente

```sh
conda env remove -n <env_name>
```

<br>

## Gerenciando de Pacotes em um Ambiente Conda

### Pacotes Recomendados

* pandas

* matplotlib

### Instalação de um Novo Pacote

* Ativar um ambiente já previamente criado:

  ```sh
  conda activate <env_name>
  ```

* Instalar o pacote (_lib_)

  ```sh
  conda install <lib_name>[=version]
  ```

  * Exemplo

    ```sh
    conda install python=3.9.12
    conda install numpy
    ```

* Exportar a lista de pacotes de um ambiente para um arquivo

  ```sh
  conda env export > environment.yml
  ```

* Recriar um ambiente a partir do arquivo `environment.yml`

  ```sh
  conda env create -f environment.yml
  ```

<br>

## Instalação do Jupyter Lab (Linux/Ubuntu) através do Conda

* Ativar um ambiente

  ```sh
  conda activate <env_name>
  ```

* Instalar o Jupyter Lab

  ```sh
  conda install jupyterlab
  ```

  ou, caso não tenha configurado o repositório `conda-forge`:

  ```sh
  conda install -c conda-forge jupyterlab
  ```

## Instalação de um Kernel no Jupyter

### Método 1: Mais simples

* Instalar o `nb_conda_kernels` no ambiente base:

```sh
conda install -c conda-forge nb_conda_kernels
```

* Instalar o ambiente `env` como kernel do Jupyter:

```sh
conda activate <env_name>
conda install ipykernel
conda deactivate
```

### Método 2: Kernels Individuais

```sh
conda activate <env_name>
conda install ipykernel
ipython kernel install --user --name=<kernel_name>
conda deactivate
```

<br>

## Links

* https://nbviewer.jupyter.org/
* https://nbviewer.jupyter.org/github/bokeh/bokeh-notebooks/blob/main/tutorial/06%20-%20Linking%20and%20Interactions.ipynb
* https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks
* https://github.com/rasbt/algorithms_in_ipython_notebooks
* https://nbviewer.jupyter.org/github/jrjohansson/scientific-python-lectures/blob/master/Lecture-4-Matplotlib.ipynb
* https://www.dataschool.io/cloud-services-for-jupyter-notebook/

<br>

| Thumb | Descrição |
| :-: | --- |
| [![img](https://img.youtube.com/vi/8laFJI2l3gU/default.jpg)](https://www.youtube.com/watch?v=8laFJI2l3gU) | <sup>[Ciência Programada]</sup> [__Criando um ambiente virtual para seu projeto Python__](https://www.youtube.com/watch?v=8laFJI2l3gU) <br> <sub>(1:18:40, YouTube, Ago/2020)</sub>

<br>
