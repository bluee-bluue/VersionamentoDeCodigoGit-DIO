# Versionamento de Código com Git e GitHub

Comandos do Git ensinados no curso Versionamento de Código com Git e GitHub da [Digital Innovation One](https://wwwdio.me/), e também em pesquisas e outros recursos.

##
### 📚 Documentação
- [Documentação Git](https://git-scm.com/doc)
- [Documentação GitHub](https://docs.github.com/)

##
### 💻 Comandos

| Ação | Como usar |
|-------|---------|
| Configuração do Git | [Como usar](#configuração-do-git) |
| Primeiro commit | [Como usar](#primeiro-commit) |
| Remoção | [Como usar](#remoção) |
| Atualizar commit | [Como usar](#atualizar-commit) |
| Ignorar pastas ou arquivos | [Como usar](#ignorar-pastas-ou-arquivos) |
| Comandos importantes do git | [Como usar](#comandos-importantes-do-git) |
| Puxando alterações | [Como usar](#puxando-alterações) |
| Branches | [Como usar](#branches) |
| Tags | [Como usar](#tags) |

##
### - Configuração do Git
```bash
git config --global user.email {email}      # Definir/Alterar email
git config --global user.nome {nome}        # Definir/Alterar nome
git config --global core.longpaths true     # Definir/Alterar tamanho de diretórios
```


### - Primeiro commit
```bash
git init                                    # Inicializa um novo repositório local
git add . ou {nome do arquivo}              # Adiciona arquivos modificados ao palco
git commit -m "mensagem"                    # Realiza o commit dos arquivos modificados
git branch -m {nome da branch}              # Renomear a branch atual
git remote add origin {link do repositório} # Adiciona o link do repositório remoto ao repositório local
git push -u origin {nome da branch}         # Realiza o primeiro envio envio das modificações
```

### - Remoção
```bash
git rm -r --cached {nome da pasta}  # Remove a pasta e seus arquivos
git rm --cached {nome do arquivo}   # Remove o arquivo
rm -r .git/                         # Remove o repositório local
```

### - Atualizar commit
```bash
git add . ou {nome do arquivo}      # Adiciona arquivos modificados ao palco
git commit -m "mensagem"            # Realiza o commit dos arquivos modificados
git push -u origin main             # Realiza o envio do commit para o repositório remoto
```

### - Ignorar pastas ou arquivos
```bash
touch .gitignore                            # Cria o arquivo .gitignore
echo "{nome do arquivo}" >> .gitignore      # Adiciona o arquivo ao .gitignore
echo "{nome da pasta/}" >> .gitignore       # Adiciona a pasta ao .gitignore
```
<small>Nota: o comando ```touch``` só funciona no terminal Bash, o terminal normal não reconhece esse comando.</small>

### - Comandos importantes do git
```bash
git restore nomeDoArquivo                                                   # Restaura o arquivo do commit
###
git commit --amend -m "mensagem"                                            # Realiza mudança na mensagem do commit
###
git log                                                                     # Lista todos os commits
git reset --soft {codigo do commit}                                         # Retorna ao commit anterior
###
git reset . ou {nomeDoArquivo}                                              # Remove o arquivo do commit
git restore --staged {nomeDoArquivo}                                        # Restaura o arquivo do commit
###
git clone {link do repositório} --branch {nome da branch} --single-branch   # Clonar branch de um repositório especifico
###
git diff --staged                                                           # Lista as alterações que serão incluídas no próximo commit
###
git commit -sm "mensagem"                                                   # Realiza o commit com sua assinatura
git commit -s                                                               # Realiza o commit com sua assinatura sem uma mensagem

```

### - Puxando alterações
```bash
git pull
```

### - Branches
```bash
git branch -v                                       # Lista todos os commits de cada branch
git branch                                          # Lista todas as branches
git branch {nome da nova branch}                    # Cria a nova branch
git checkout {nome da branch}                       # Muda para a branch
git checkout -b {nome da nova branch}               # Muda para a nova branch
git branch -d {nome da branch}                      # Remove a branch
git merge {nome da outra branch}                    # Mescla as branches
git diff {nome da branch} {nome da outra branch}    # Visualiza as diferenças entre as branches. Exemplo: git diff main origin/main
```
<small>Nota: O comando ```git checkout -b``` além de criar uma nova branch, também realiza a troca automatica sem precisar de um novo comando.</small>

### - Tags
```bash
git tag                                     # Lista todas as tags
git tag -a {nome da tag} -m "mensagem"      # Cria uma nova tag
git tag -d {nome da tag}                    # Remove a tag
```

##
### 🔍 Referências
- [Git - Reference](https://git-scm.com/docs/)
- [Digital Innovation One](https://wwwdio.me/)
