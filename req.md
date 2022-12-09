# Install miniforge with mamba

curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-$(uname)-$(uname -m).sh"
bash Mambaforge-$(uname)-$(uname -m).sh

mamba create -n apm-env
mamba activate -n apm-env


# Install Dependencies

mamba install -c pytorch pytorch==1.12.1 torchvision==0.13.1 torchaudio==0.12.1
mamba install -c conda-forge cudatoolkit=11.6 
mamba install -c fastchan fastai
mamba install -c fastai fastbook 
mamba install -c conda-forge ipykernel --update-deps
mamba install -c conda-forge ipywidgets

pip install duckduckgo_search
pip install fastcore

# Lesson 4
pip install kaggle
pip install protobuf==3.20.0

provavelmente desnecessario: mamba install -c nvidia pytorch-cuda=11.6