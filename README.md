# myjupyter


## pipenv

```
sudo apt install python3-pip -y
pip3 install --user pipenv
pipenv --python 3.8
pipenv shell
pipenv install flask==0.12.1
pipenv install pytest --dev
pipenv lock
```

## jupyterlab

```
pip3 install --user dask jupyterlab
pip3 install dask_labextension
jupyter labextension install dask-labextension
jupyter serverextension enable dask_labextension
jupyter labextension install @jupyter-widgets/jupyterlab-manager
jupyter labextension install @bokeh/jupyter_bokeh
sudo apt install graphviz
pip3 install numpy pandas h5py scikit-image
pip3 install --upgrade jupyterlab-git
jupyter lab build
jupyter serverextension enable --py jupyterlab_git
```