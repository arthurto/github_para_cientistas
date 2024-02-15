# Comandos e sintaxe do Git

## Configuração Inicial

- **`git config --global user.name "Seu Nome"`**
  - Configura o nome que aparecerá em suas contribuições.
- **`git config --global user.email "seuemail@exemplo.com"`**
  - Configura o email que será associado às suas contribuições.


## Criando e Clonando Repositórios
Com o git podemos criar um repositório ou 'clonar' um repositório existente disponível no GitHub. 

- **`git init`**
  - Inicializa um novo repositório Git local.
- **`git clone git@github.com:usuario/repositorio.git`**
  - Faz uma cópia local de um repositório Git remoto usando SSH. Isso requer que você tenha configurado as chaves SSH para sua conta no GitHub.

## Trabalhando com Alterações

- **`git status`**
  - Mostra o estado atual do repositório, incluindo alterações não rastreadas.
- **`git add .` ou `git add nome_do_arquivo`**
  - Adiciona arquivos ao próximo commit. Use `.` para adicionar todas as alterações.
- **`git commit -m "Mensagem do commit"`**
  - Salva as alterações no repositório com uma mensagem descrevendo o que foi feito.
- **`git push origin nome_da_branch`**
  - Envia as alterações para o repositório remoto.
- **`git pull`**
  - Atualiza o repositório local com as alterações do repositório remoto.

## Branching e Merging

- **`git branch`**
  - Lista todas as branches locais. Adicione `-a` para ver todas as branches (locais e remotas).
- **`git branch nome_da_nova_branch`**
  - Cria uma nova branch.
- **`git checkout nome_da_branch`**
  - Muda para a branch especificada.
- **`git merge nome_da_branch`**
  - Une a branch especificada à branch atual.

## Desfazendo Alterações

- **`git checkout -- nome_do_arquivo`**
  - Descarta alterações em um arquivo específico.
- **`git reset HEAD nome_do_arquivo`**
  - Remove um arquivo da área de staging (área de preparação), mas preserva suas alterações.
- **`git reset --hard`**
  - Desfaz todas as alterações locais, revertendo para o último estado do repositório.

