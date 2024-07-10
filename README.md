# OpenChat
# Tentativa de Uso do OpenChat  

Este projeto descreve as tentativas de uso do servidor deste ChatBot de Código Aberto, feito por uma aluna do curso de Tópicos em Sistemas Digitais. 

Consulte **[Pré-requisitos](#-Pr%C3%A9-requisitos)** para saber como implantar o projeto.

## 🚀 Começando

Antes de tudo, prepare o seu ambiente Linux. 
Primeiramente, eu tentei com máquina virtual do Oracle e não obtive muito sucesso devido à uma série de limitações, como tamanho de memória sempre fixo (no ato de criação da máquina) e o não reconhecimento da minha placa de vídeo (AMD RADEON 7). 
Assim, recomendo que instale sua distro linux realizando DUAL boot em seu computador, ou utilizando o WSL dentro do Windows. Vi muita gente conseguindo obter sucesso ao utilizar o WSL.  
Aqui está um link de como instalar o OpenChat usando WSL <https://github.com/imoneoi/openchat/issues/41#issuecomment-1798297382>. 
Se for utilizar DUAL boot, pode prosseguir neste documento. 



### 📋 Pré-requisitos

Antes de qualquer coisa, instale o ambiente conda, ele isola as variáveis e demais arquivos, além de você obter um maior controle de qual versão de biblioteca e de interpretador está utilizando. 

Siga as instruções do próprio site do Conda: 

<https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html>


### 🔧 Criação do Ambiente Conda 

Após a instalação, aplique as alterações fechando e abrindo o terminal, ou executando o comando a seguir: 

```
source ~/.bashrc

```

Comece criando e instalando a versão correta do Interpretador Python: 

```
conda create --name my_env python=3.11
```
E depois abra-o: 


### 🔧 Instalação

Como obtive muitos erros ao tentar ir direto à instalação do OpenChat, comece instalando pacotes no seu computador:


```
sudo apt-get install git
```

E repita:

```
Até finalizar
```

Termine com um exemplo de como obter dados do sistema ou como usá-los para uma pequena demonstração.

## ⚙️ Executando os testes

Explicar como executar os testes automatizados para este sistema.

### 🔩 Analise os testes de ponta a ponta

Explique que eles verificam esses testes e porquê.

```
Dar exemplos
```

### ⌨️ E testes de estilo de codificação

Explique que eles verificam esses testes e porquê.

```
Dar exemplos
```

## 📦 Implantação

Adicione notas adicionais sobre como implantar isso em um sistema ativo

## 🛠️ Construído com

Mencione as ferramentas que você usou para criar seu projeto

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - O framework web usado
* [Maven](https://maven.apache.org/) - Gerente de Dependência
* [ROME](https://rometools.github.io/rome/) - Usada para gerar RSS

## 🖇️ Colaborando

Por favor, leia o [COLABORACAO.md](https://gist.github.com/usuario/linkParaInfoSobreContribuicoes) para obter detalhes sobre o nosso código de conduta e o processo para nos enviar pedidos de solicitação.

## 📌 Versão

Nós usamos [SemVer](http://semver.org/) para controle de versão. Para as versões disponíveis, observe as [tags neste repositório](https://github.com/suas/tags/do/projeto). 

## ✒️ Autores

Mencione todos aqueles que ajudaram a levantar o projeto desde o seu início

* **Um desenvolvedor** - *Trabalho Inicial* - [umdesenvolvedor](https://github.com/linkParaPerfil)
* **Fulano De Tal** - *Documentação* - [fulanodetal](https://github.com/linkParaPerfil)

Você também pode ver a lista de todos os [colaboradores](https://github.com/usuario/projeto/colaboradores) que participaram deste projeto.

## 📄 Licença

Este projeto está sob a licença (sua licença) - veja o arquivo [LICENSE.md](https://github.com/usuario/projeto/licenca) para detalhes.

## 🎁 Expressões de gratidão

* Conte a outras pessoas sobre este projeto 📢;
* Convide alguém da equipe para uma cerveja 🍺;
* Um agradecimento publicamente 🫂;
* etc.


---
⌨️ com ❤️ por [Armstrong Lohãns](https://gist.github.com/lohhans) 😊
