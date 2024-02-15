# Git/GitHub para Cientistas

Este repositório tem como objetivo introduzir os conceitos chave iniciais para 
que o Git e o GitHub (ou alternativos, como GitLab) sejam utilizados pela comunidade 
científica que costumeiramente colabora no desenvolvimento de programas em diversas linguagens. 

As ferramentas utilizadas serão especificamente o Git e o GitHub, ferramentas extensamente utilizada 
pela comunidade desenvolvedora de software. 

# Organização do Repositório 

Este reposiório está organizado da seguinte maneira:

- [01 - Comandos e Sintaxe](comandos.md)
- [02 - Protocolo SSH](ssh_keys.md)

## O que é o Git 

O Git não é um acrônimo, ele é porém um sistema de controle de versão distribuído. 
Ele permite a colaboração múltipla e distribuída no desenvolvimento de software (qualquer arquivo que pode ser editado em texto).
Sendo distribuído, cada desenvolvedor possui uma versão local do programa. 
As mudanças podem ser feitas localmente e em seguida sincronizadas com o repositório central (GitHub).

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


