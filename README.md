# Git/GitHub para Cientistas

Este repositório tem como objetivo introduzir os conceitos iniciais para a utilização do 
 Git e do GitHub (ou alternativos, como GitLab). O Git e o GitHub são ferramentas de desenvolvimento 
 colaborativas, que permitem que os arquivos sejam compartilhados, testados, editados e mantivos em grupo de forma 
 assíncrona e distribuída.

As ferramentas utilizadas serão especificamente o Git e o GitHub, ferramentas extensamente utilizada 
pela comunidade desenvolvedora de software. O Git e o GitHub são a peças fundamentais no funcionamento de 
muitos projetos particulares e públicos de software. Ele foi desenvolvido por Linus Torvalds, e o seu desenvolvimento foi auxiliado por ele próprio. O git foi feito com ajuda do git. 

## Conceitos fundamentais 

O git mantém os arquivos de uma pasta, ou repositório raiz, em `branches` ou ramificações. A branch principal é comummente chamada de `main`. Para começar a fazer o `tracking` das mudanças de um reposiótio é necessário utilizar o comando `git init` no repositório pelo terminal. Para adicionar os arquivos atuais no ramo principal precisamos utilizar os comandos `git add .` e em seguida `git commit -m "mensagem relevante (ou primeiro commit, nesse caso)"`, a mensagem pode ser qualquer.

Dessa forma podemos começar a colocar diferentes arquivos, a cada commit as alterações novas são salvas e podem ser revertidas.

# Organização do Repositório 

Este reposiório está organizado da seguinte maneira:

- [01 - Comandos e Sintaxe](comandos.md)
- [02 - Protocolo SSH](ssh_keys.md)

## O que é o Git 

Git não é um acrônimo, ele é porém um sistema de controle de versão distribuído. 
Ele permite a colaboração múltipla e distribuída no desenvolvimento de software.
Sendo distribuído, cada desenvolvedor possui uma versão local do programa e de suas possíveis `branches`, ou ramificações. 
As mudanças podem ser feitas localmente e em seguida sincronizadas com o repositório central (GitHub).

### Início de um projeto e o "começo da história"

Digamos que um projeto seu esteja em uma pasta, ou repositório. Com o Git instalado, você pode inciar um reposiório git executando
```bash 
git init
```
Isso criará um repositório git, criará um subdiretório `.git` com todos os arquivos necessários para o controle de versão do projeto. 
A partir desse comando você poderar comçar a utilizar as funcionalidades do git para rastrear os arquivos localmente, ou manter o controle sobre as 
diferentes versões que ele vai ter.

Após isso podemos utilizar o comando:
```bash 
git add . 
git commit -m "primeiro commit"
```
Isso coloca todos os arquivos presentes no repositório em "staging" e depois esses arquivos são "commitados".
O comando `add` é responsável pelo "staging", que é um estágio de preparação, o comando seguinte, `commit` é responsável
por "salvar" o estágio atual do desenvolvimento, os arquivos e suas mudanças, na história do projeto. 

### Diferentes ramifiações

Todo projeto possui um "ramo central", ou "branch". Normalmente esse branch é chamado de `main` ou `master`. 
Esse é o ramo principal, que possui, por convenção e por estrutura, a versão principal dos arquivos do projeto. 
Podemos criar ramificações do ramo principal utilizando o comando
```bash 
git branch nome_do_novo_branch
```


e depois mudar para o novo ramo
```bash 
git checkout nome_do_novo_branch
```
para que os próximos comandos `add` e `commit` tenham efeito sobre ele e não sob o principal.

Existem outros comandos, mas esses são os mais básicos. 
Assim você pode controlar diferentes versões de código localmente. 


## Repositórios remotos e colaboração 

O GitHub (ou GitLab) permite que você colabore através de um repositório remoto.
Um repositório remoto pode ser adicionado com o comando `git remote add link_do_repositório`.

### Baixando e instalando o Git 

#### Windows

1. Acesse [git-scm.com](https://git-scm.com/) e clique em "Download" para a versão Windows.
2. Execute o arquivo baixado e siga as instruções de instalação.

#### macOS

- **Homebrew**: Execute `brew install git` no Terminal.
- **Instalador Oficial**: Baixe do [git-scm.com](https://git-scm.com/) e siga as instruções de instalação.

#### Linux

- **Debian/Ubuntu**: Execute `sudo apt-get update` seguido de `sudo apt-get install git`.
- **Fedora**: Execute `sudo dnf install git`.
- **CentOS/RHEL**: Execute `sudo yum install git`.

Verifique a instalação com `git --version`.


