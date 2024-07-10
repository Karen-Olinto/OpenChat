# OpenChat
# Tentativa de Uso do OpenChat  

Este projeto descreve as tentativas de uso do servidor deste ChatBot de Código Aberto, feito por uma aluna do curso de Tópicos em Sistemas Digitais. 

Consulte **[Pré-requisitos](#-Pr%C3%A9-requisitos)** para começar a implantar o projeto.

## 🚀 Começando

Antes de tudo, prepare o seu ambiente Linux. 

Primeiramente, eu tentei com máquina virtual do Oracle e não obtive muito sucesso devido à uma série de limitações, como tamanho de memória sempre fixo (no ato de criação da máquina) e o não reconhecimento da minha placa de vídeo (AMD RADEON 7). 

Assim, recomendo que instale sua distro-linux realizando dualboot em seu computador, ou utilizando o WSL dentro do Windows. Vi muita gente conseguindo obter sucesso ao utilizar o WSL.  

Aqui está um exemplo de sucesso usando WSL <https://github.com/imoneoi/openchat/issues/41#issuecomment-1798297382>. 



### 📋 Pré-requisitos

Antes de qualquer coisa, instale o ambiente conda, ele isola as variáveis e demais arquivos, além de você obter um maior controle de qual versão de biblioteca e de interpretador está utilizando. 

Siga as instruções do próprio site do Conda: 

<https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html>


### 🔧 Criação do Ambiente Conda 

Após a instalação, aplique as alterações fechando e abrindo o terminal, ou executando o comando a seguir: 

```
source ~/.bashrc

```

Comece criando o ambiente e instalando a versão correta do Python: 

```
conda create --name my_env python=3.11
```

E depois abra-o: 

```
conda activate my_env
```


### 🔧 Instalação

Como obtive muitos erros ao tentar ir direto à instalação do OpenChat, comece instalando pacotes no seu computador:


```
sudo apt-get install git
```

E pacotes do python também:

```
pip3 install packaging ninja
```

E atualizar o compilador g++:

```
sudo apt update
sudo apt install build-essential
```

E se você for usar GPU NVIDIA (ou outra sem ser AMD) talvez seja útil ir por esse caminho: 
```
conda install -y cudatoolkit-dev -c conda-forge
```

E independemente, continue instalando a seguir: 
```
// pip3 install torch torchvision torchaudio
pip install torch==2.0.1 torchvision==0.15.2 torchaudio==2.0.2 --index-url https://download.pytorch.org/whl/cu118
```

E finalmente, 
```
pip3 install --no-build-isolation "flash-attn<2"
pip3 install ochat
```


## ⚙️ Executando os testes

Teste de uso do servidor que funciona com as pessoas, após a instalação ser bem sucedida: 

```
python -m ochat.serving.openai_api_server --model openchat/openchat_3.5 --tensor-parallel-size 1
```


## 🛠️ Construído com

Há mais testes disponíveis na página oficial: 

* [OpenChat](https://github.com/imoneoi/openchat) 


## 📌 Versão

Nesta data, 10 de julho de 2024, as versões atuais são:


 packages in environment at /home/karen/anaconda3/envs/my_env:

  Name                    Version                   Build  Channel  <br>
_libgcc_mutex             0.1                        main  <br>
_openmp_mutex             5.1                       1_gnu  <br>
absl-py                   2.1.0                    pypi_0    pypi <br>
astunparse                1.6.3                    pypi_0    pypi <br>
bzip2                     1.0.8                h5eee18b_6  <br>
ca-certificates           2024.3.11            h06a4308_0  <br>
cachetools                5.3.3                    pypi_0    pypi <br>
certifi                   2024.7.4                 pypi_0    pypi <br>
charset-normalizer        3.3.2                    pypi_0    pypi <br>
filelock                  3.15.4                   pypi_0    pypi <br>
flatbuffers               24.3.25                  pypi_0    pypi <br>
fsspec                    2024.6.1                 pypi_0    pypi <br>
gast                      0.6.0                    pypi_0    pypi <br>
google-auth               2.32.0                   pypi_0    pypi <br>
google-auth-oauthlib      1.0.0                    pypi_0    pypi <br>
google-pasta              0.2.0                    pypi_0    pypi <br>
grpcio                    1.64.1                   pypi_0    pypi <br>
h5py                      3.11.0                   pypi_0    pypi <br>
idna                      3.7                      pypi_0    pypi <br>
jinja2                    3.1.4                    pypi_0    pypi <br>
keras                     2.14.0                   pypi_0    pypi <br>
ld_impl_linux-64          2.38                 h1181459_1   <br>
libclang                  18.1.1                   pypi_0    pypi <br>
libffi                    3.4.4                h6a678d5_1  <br>
libgcc-ng                 11.2.0               h1234567_1  <br>
libgomp                   11.2.0               h1234567_1  <br>
libstdcxx-ng              11.2.0               h1234567_1  <br>
libuuid                   1.41.5               h5eee18b_0  <br>
markdown                  3.6                      pypi_0    pypi <br>
markupsafe                2.1.5                    pypi_0    pypi <br>
ml-dtypes                 0.2.0                    pypi_0    pypi <br>
mpmath                    1.3.0                    pypi_0    pypi <br>
ncurses                   6.4                  h6a678d5_0  <br>
networkx                  3.3                      pypi_0    pypi <br>
ninja                     1.11.1.1                 pypi_0    pypi <br>
numpy                     2.0.0                    pypi_0    pypi <br>
nvidia-cublas-cu12        12.1.3.1                 pypi_0    pypi <br>
nvidia-cuda-cupti-cu12    12.1.105                 pypi_0    pypi <br>
nvidia-cuda-nvrtc-cu12    12.1.105                 pypi_0    pypi <br>
nvidia-cuda-runtime-cu12  12.1.105                 pypi_0    pypi <br>
nvidia-cudnn-cu12         8.9.2.26                 pypi_0    pypi <br>
nvidia-cufft-cu12         11.0.2.54                pypi_0    pypi <br>
nvidia-curand-cu12        10.3.2.106               pypi_0    pypi <br>
nvidia-cusolver-cu12      11.4.5.107               pypi_0    pypi <br>
nvidia-cusparse-cu12      12.1.0.106               pypi_0    pypi <br>
nvidia-nccl-cu12          2.20.5                   pypi_0    pypi <br>
nvidia-nvjitlink-cu12     12.5.82                  pypi_0    pypi <br>
nvidia-nvtx-cu12          12.1.105                 pypi_0    pypi <br>
oauthlib                  3.2.2                    pypi_0    pypi <br>
openssl                   3.0.14               h5eee18b_0   <br>
opt-einsum                3.3.0                    pypi_0    pypi <br>
packaging                 24.1                     pypi_0    pypi <br> 
pillow                    10.4.0                   pypi_0    pypi <br>
pip                       24.0                     pypi_0    pypi <br>
protobuf                  4.25.3                   pypi_0    pypi <br>
pyasn1                    0.6.0                    pypi_0    pypi <br>
pyasn1-modules            0.4.0                    pypi_0    pypi <br>
python                    3.11.9               h955ad1f_0  <br>
readline                  8.2                  h5eee18b_0  <br>
requests                  2.32.3                   pypi_0    pypi <br>
requests-oauthlib         2.0.0                    pypi_0    pypi <br>
rsa                       4.9                      pypi_0    pypi <br>
setuptools                69.5.1                   pypi_0    pypi <br>
six                       1.16.0                   pypi_0    pypi <br>
sqlite                    3.45.3               h5eee18b_0  <br>
sympy                     1.12.1                   pypi_0    pypi <br> 
tensorboard               2.14.1                   pypi_0    pypi <br>
tensorboard-data-server   0.7.2                    pypi_0    pypi <br>
tensorflow-estimator      2.14.0                   pypi_0    pypi <br>
tensorflow-io-gcs-filesystem 0.37.1                   pypi_0    pypi <br>
tensorflow-rocm           2.14.0.600               pypi_0    pypi <br>
termcolor                 2.4.0                    pypi_0    pypi <br>
tk                        8.6.14               h39e8969_0  <br>
torch                     2.3.1                    pypi_0    pypi <br>
torchaudio                2.3.1                    pypi_0    pypi <br>
torchvision               0.18.1                   pypi_0    pypi <br>
triton                    2.3.1                    pypi_0    pypi <br>
typing-extensions         4.12.2                   pypi_0    pypi <br>
tzdata                    2024a                h04d1e81_0  <br>
urllib3                   2.2.2                    pypi_0    pypi <br>
werkzeug                  3.0.3                    pypi_0    pypi <br>
wheel                     0.43.0                   pypi_0    pypi <br>
wrapt                     1.14.1                   pypi_0    pypi <br>
xz                        5.4.6                h5eee18b_1  <br>
zlib                      1.2.13               h5eee18b_1  <br>



## ✒️ Autores

Karen da Silva Olinto
---
⌨️ E este modelo de README.md ❤️ por [Armstrong Lohãns](https://gist.github.com/lohhans) 😊
