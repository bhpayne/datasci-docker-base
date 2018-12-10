# Virtualbox

# Jupyter

# Octave Jupyter
https://hub.docker.com/r/compdatasci/octave-jupyter/

```
docker run --rm -ti -w/home/compdatasci/shared -v $(pwd):/home/compdatasci/shared \
-d -p $(docker-machine ip $(docker-machine active)):8088:8088 \
compdatasci/octave-jupyter:latest
```

https://github.com/compdatasci/docker-jupyter/tree/master/octave-jupyter
```
docker run --rm -w /home/compdatasci/shared -v $(pwd):/home/compdatasci/shared -d -p \
    $(docker-machine ip $(docker-machine active)):8088:8088 compdatasci/octave-jupyter \
    'jupyter-notebook --no-browser --ip=0.0.0.0 --port=8088'
```


# Jupyter datascience
https://hub.docker.com/r/jupyter/datascience-notebook/
```
docker run -p 8888:8888  -v "$PWD":/home/jovyan jupyter/datascience-notebook
```

https://www.dataquest.io/blog/docker-data-science/
https://jupyter-docker-stacks.readthedocs.io/en/latest/using/recipes.html#using-pip-install-or-conda-install-in-a-child-docker-image

******************

https://jupyter-docker-stacks.readthedocs.io/en/latest/using/recipes.html#run-jupyterlab
```
docker run -it -e JUPYTER_ENABLE_LAB=yes -p 8888:8888 --net=dockernet  -v "$PWD":/home/jovyan datasci start.sh jupyter lab --LabApp.token=''
```

## C in Jupyter
C in Jupyter:
https://hub.docker.com/r/brendanrius/jupyter-c-kernel/
https://libraries.io/github/brendan-rius/jupyter-c-kernel
```
docker pull brendanrius/jupyter-c-kernel
docker run -p 8888:8888 brendanrius/jupyter-c-kernel
```
## jupyterlab

https://hub.docker.com/r/mikebirdgeneau/jupyterlab/
https://github.com/mikebirdgeneau/jupyterlab-docker/blob/master/jupyterlab/Dockerfile

## jupyter Spark
https://hub.docker.com/r/jupyter/all-spark-notebook/
```
docker pull jupyter/all-spark-notebook
```

```
docker run -p 8888:8888  -v "$PWD":/home/jovyan jupyter/all-spark-notebook
```

```
docker run -it --rm -p 8888:8888                jupyter/all-spark-notebook
```
Has scala

https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html

https://github.com/jupyter/docker-stacks/tree/master/all-spark-notebook
how to use:
https://github.com/Paperspace/jupyter-docker-stacks/tree/master/all-spark-notebook
https://jupyter-docker-stacks.readthedocs.io/en/latest/using/specifics.html

https://blog.sicara.com/get-started-pyspark-jupyter-guide-tutorial-ae2fe84f594f

# Powershell
https://hub.docker.com/r/microsoft/powershell/

# Neo4j
https://hub.docker.com/_/neo4j/
```
docker pull neo4j
```

```
docker run \
    --publish=7474:7474 --publish=7687:7687 \
    --volume=$HOME/neo4j/data:/data \
    --env=NEO4J_AUTH=none \
    neo4j
```

# OrientDB
https://hub.docker.com/_/orientdb/
```
docker run -d --name orientdb -p 2424:2424 -p 2480:2480 -e ORIENTDB_ROOT_PASSWORD=rootpwd orientdb
```
# Cytoscape
https://hub.docker.com/u/cytoscape/
https://hub.docker.com/r/cytoscape/jupyter-cytoscape/
```
docker pull cytoscape/jupyter-cytoscape
```
```
docker run -d -p 8888:8888 cytoscape/jupyter-cytoscape start-notebook.sh --NotebookApp.token=''
```
http://localhost:8888/notebooks/examples/smallNetwork/smallNetwork.ipynb

```
jupyter nbextension enable --py --sys-prefix widgetsnbextension
```

# valgrind and gdb in Ubuntu
gcc+valgrind+gdb
https://hub.docker.com/_/gcc/
https://github.com/docker-library/gcc

```
docker run -it gcc:latest
```
--> gdb is not installed
--> valgrind is not installed

```
cd ubuntu
docker build -t ubunt .
```

# python3
https://hub.docker.com/_/python/

```
docker run python:3
```
```
docker run -it python:3 bash -c bash
docker run -it python:3 bash -c python3
```

```
docker run -it -v "$PWD":/scripts -w /scripts python:3 bash -c bash
```
-v maps the host directory to the image's "scripts" directory
-w opens the image in /scripts in the image

****************
# Latex
https://hub.docker.com/r/blang/latex/
```
docker run blang/latex
```
