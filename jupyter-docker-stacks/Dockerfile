FROM  jupyter/scipy-notebook:latest
LABEL maintainer="Motuzov <motuzov@gmail.com>"

USER root

RUN apt-get update --yes && \
    apt-get install --yes --no-install-recommends \
    vim && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

USER ${NB_UID}

# Install dsml4s8e libs
RUN  mamba install --name base pycodestyle gitpython papermill ipynbname dagster dagstermill dagit -y && \
     mamba clean --all -f -y && \
     fix-permissions "${CONDA_DIR}" && \
     fix-permissions "/home/${NB_USER}"

RUN pip install torch torchvision pyarrow pytorch-lightning optuna pytorch-forecasting && \
    pip install -U pytest 

USER ${NB_UID}

WORKDIR "${HOME}"
