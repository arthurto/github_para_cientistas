# Cadastrando Chaves SSH no GitHub em Linux

Este tutorial o guiará através do processo de geração de uma chave SSH no Linux e de seu cadastro no GitHub, permitindo uma conexão segura sem a necessidade de digitar seu nome de usuário e senha a cada operação.

## Passo 1: Verificar a Existência de Chaves SSH

Antes de gerar uma nova chave SSH, verifique se você já possui alguma no seu sistema.

```bash
ls -al ~/.ssh
```


Procure por arquivos nomeados `id_rsa.pub` ou `id_ed25519.pub`. 
Se algum desses arquivos existir, você já tem uma chave SSH e pode optar por usá-la ou gerar uma nova.

## Passo 2: Gerar uma Nova Chave SSH

Se você decidir gerar uma nova chave SSH, use o seguinte comando:

```bash
ssh-keygen -t ed25519 -C "seu_email@example.com"
```

Substitua `"seu_email@example.com"` pelo seu email. 
## Passo 3: Adicionar a Chave SSH ao ssh-agent
Inicie o ssh-agent em background e adicione sua chave SSH privada ao ssh-agent.

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

## Passo 4: Adicionar a Chave SSH ao GitHub

Copie a chave SSH para a sua área de transferência:
```bash
cat ~/.ssh/id_ed25519.pub
```

No GitHub, acesse `Settings > SSH and GPG keys > New SSH key`.
No campo "Title", adicione um descrição para a chave.
No campo "Key", cole a chave SSH que você copiou.
Clique em `Add SSH key`.
## Passo 5: Testar a Conexão
Após adicionar sua chave SSH ao GitHub, teste a conexão:

```bash
ssh -T git@github.com
```

Agora está tudo pronto para clonar repositórios privados, próprios ou de terceiros com
a devida autorização (ser aceito ou adicionado como colaborador).
