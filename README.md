# myjupyter

```
git config user.email "basdemir@gmail.com"
git config user.name "Serkan Basdemir"
```

## pipenv

```
sudo apt install graphviz python3-pip -y
pip install pipenv
pipenv --python 3.8
pipenv shell
pipenv install flask==0.12.1
pipenv install pytest --dev
pipenv lock
```

## jupyterlab

```
pip install dask jupyterlab
pip install dask_labextension
pip install s3fs
jupyter labextension install dask-labextension
jupyter serverextension enable dask_labextension
jupyter labextension install @jupyter-widgets/jupyterlab-manager
jupyter labextension install @bokeh/jupyter_bokeh
pip install numpy pandas h5py scikit-image
pip install --upgrade jupyterlab-git
jupyter lab build
jupyter serverextension enable --py jupyterlab_git
```

## To Install minio on k8s
```
k create ns minio
kubens minio
helm repo add minio https://helm.min.io/
helm install minio minio/minio --set service.type=NodePort,accessKey=abcdefgh,secretKey=abcdefgh
```

## To Install minio on docker

docker run -d -p 9000:9000 \
  --name minio-server \
  -v /mnt/data:/data \
  -e "MINIO_ACCESS_KEY=abcdefgh" \
  -e "MINIO_SECRET_KEY=abcdefgh" \
  minio/minio server /data