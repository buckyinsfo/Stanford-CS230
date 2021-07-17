FROM jupyter/scipy-notebook

USER root

RUN apt-get update && \
    apt-get install -y octave gnuplot && \
    apt-get clean && rm -rf var/lib/apt/lists/*

USER $NB_UID

RUN pip install torch && \
    pip install --no-deps torchvision && \
    pip install octave-kernel gnuplot_kernel

EXPOSE 8888
CMD ["jupyter", "notebook"]
