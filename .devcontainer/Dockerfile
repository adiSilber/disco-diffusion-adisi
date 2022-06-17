FROM nvcr.io/nvidia/pytorch:21.08-py3 AS prep


ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Install a few dependencies
RUN apt update
RUN DEBIAN_FRONTEND=noninteractive TZ=Etc/UTC apt-get -y install -y tzdata imagemagick ffmpeg

# Install Python packages
RUN pip install imageio imageio-ffmpeg==0.4.4 pyspng==0.1.0 lpips datetime timm ipywidgets omegaconf>=2.0.0 pytorch-lightning>=1.0.8 torch-fidelity einops wandb pandas ftfy
