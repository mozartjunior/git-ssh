# GitHub & SSH Keys (Notes)

Instalacao do git, verificar se possui chave ssh e caso nao possua gerar chave ssh e vincular com a conta do github.\
Install git, check if you have an ssh key, if not, generate an ssh key and link it with your github account.



## Installation GitHub (Ubuntu)

Install git

```bash
  sudo apt install git
  git --version
```
## SSH-Keys

1.0 Verificar se a maquina possui chave SSH;
```bash
  ls -al ~/.ssh
```
1.1 Se retornar o resultado:
```bash
  ls: cannot access '/home/mozart/.ssh': No such file or directory
```
1.2 Gere uma chave SSH com o e-mail que voce utiliza para acessar o GitHub

```bash
  ssh-keygen -t ed25519 -C 'seu@email'
```
*Crie uma senha, essa senha voce ira utilizar todas as vezes que for utilizar o push do repositorio local para o GitHub.*

1.3 Resultado com algo parecido

```
  SHA256:mjuXXXXXXXXXXXXXXXXXXXXXXXXXX seu@email.com
The key's randomart image is:
+--[ED25519 256]--+
|=E*O=            |
|=oBo+. .         |
|.. + .o .        |
|  +   .. .       |
|   o o .S.. .    |
|    XXXXXXXX     |
|   o.+=o o.      |
|   o++=o...      |
|  ..oo+o.o       |
+----[SHA256]-----+
```
## Vincular com o GitHub
Execute o comando 1.0, o resultado mostrará as chaves geradas.

## Configurações do GitHub
Configurações>SSH and GPG Keys\
Crie uma nova chave: New SSH Key

Verificar a chave publica que voce gerou no passo 1.2
```
  cat  ~/.ssh/id_ed25519.pub
```
*Copie todo o texto e cole dentro da caixa, e Add SSH Key.*

## Validacao
Crie um repositorio no github (site), e depois faça o clone para o repositorio desejado dentro do seu PC.
```
git clone git@git.url.do.repositorio.do.site
```
*senha*

Caso de mensagem de erro: Author identity unknown

```bash
Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
```


## 🚀 About Me
Analista de Redes estudando outras áreas focalizando na migração de carreira...


![Logo](https://www.shutterstock.com/image-vector/pixel-art-8bit-business-computer-250nw-1861306273.jpg)
