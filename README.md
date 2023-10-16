# Versionamento de Código com Git e GitHub

Comandos do Git ensinados no curso Versionamento de Código com Git e GitHub da [Digital Innovation One](https://wwwdio.me/), e também em pesquisas e outros recursos.

## 📚 Documentação
- [Documentação Git](https://git-scm.com/doc)
- [Documentação GitHub](https://docs.github.com/)

## 💻 Comandos

| Ação | Como usar |
|-------|---------|
| Definir/Alterar email | [Como usar](#definiralterar-email) |
| Definir/Alterar nome | [Como usar](#definiralterar-nome) |
| Novo repositório | [Como usar](#inicializa-um-novo-repositório-local) |
| Ativar tamanhos longos de diretórios | [Como usar](#ativar-tamanhos-longos-de-diretórios) |
| Adicionar arquivos modificados | [Como usar](#adicionar-arquivos-modificados-do-palco) |
| Commit dos arquivos | [Como usar](#realiza-o-commit-dos-arquivos-mofificados) |
| Troca de branch | [Como usar](#troca-de-branch) |
| Adicionar link do repositório remoto | [Como usar](#adiciona-o-link-do-repositório-remoto-ao-repositório-local) |
| Primeiro envio das modificações | [Como usar](#realiza-o-primeiro-envio-envio-das-modificações) |
| Remover pasta ou arquivo | [Como usar](#remover-pasta-ou-arquivo-do-controle-de-versão) |
| Atualizar commit | [Como usar](#atualizar-commit) |
| .gitignore | [Como usar](#gitignore--ignorar-pastas-ou-arquivos) |
| Criar pasta | [Como usar](#criar-pasta) |
| Criar arquivo README | [Como usar](#criar-arquivo-readme) |
| Remover repositorio local | [Como usar](#remover-repositorio-local) |
| Restaurar última modificação do arquivo | [Como usar](#restaurar-última-modificação-do-arquivo) |
| Mudar mensagem do commit | [Como usar](#mudar-mensagem-do-commit) |
| Retornando ao commit anterior | [Como usar](#retornando-ao-commit-anterior) |
| Removendo arquivo do commit | [Como usar](#removendo-arquivo-do-commit) |
| Puxando alterações | [Como usar](#puxando-alterações-do-repositório-remoto-para-o-repositório-local) |
| Listar último commit de cada branch | [Como usar](#listar-último-commit-de-cada-branch) |
| Listar branches existentes | [Como usar](#listar-branches-existentes) |
| Criar novas branches | [Como usar](#criar-novas-branches) |
| Criar nova branch e mudar para a mesma | [Como usar](#criar-nova-branch-e-muda-para-a-mesma) |
| Trocar de branch | [Como usar](#trocar-de-branch) |
| Mesclar branches | [Como usar](#mesclar-branches) |
| Excluir branch | [Como usar](#excluir-branch) |
| Visualizar diferenças entre branches | [Como usar](#visualizar-diferenças-entre-branches) |
| Clonar branch de um repositório especifico | [Como usar](#clonar-branch-de-um-repositório-especifico) |
| Trabalhando com tags | [Como usar](#comandos-para-trabalhar-com-tags) |
| Visualizar alterações que serão incluídas no próximo commit | [Como usar](#visualizar-alterações-que-serão-incluídas-no-próximo-commit) |
| Assinatura em um commit | [Como usar](#assinatura-em-um-commit) |

##
### Definir/Alterar email
```
git config --global user.email {email}
```
##
### Definir/Alterar nome
```
git config --global user.nome {nome}
```
##
### Inicializa um novo repositório local
```
git init
```

##
### Ativar tamanhos longos de diretórios
´´´
git config --global core.longpaths true
´´´

##
### Adicionar arquivos modificados do palco
```
git add . ou {nome do arquivo}
```

##
### Realiza o commit dos arquivos mofificados
```
git commit -m "mensagem"
```

##
### Modificar branch
```
git branch -m main
```

<small>Nota: git branch -m main deve ser usado apenas quando você deseja renomear de 'master' para 'main'.</small>

##
### Adiciona o link do repositório remoto ao repositório local
```
git remote add origin {link do repositório}
```

##
### Realiza o primeiro envio envio das modificações
```
git push -u origin main
```

<small>Nota: Aos demais envio de modificações, usar apenas ```git push```.</small>

##
### Remover pasta ou arquivo do controle de versão
```
git rm -r --cached {nome da pasta}
```
ou
```
git rm --cached {nome do arquivo}
```
##
### Atualizar commit
```
git add . ou {nome do arquivo}
git commit -m "mensagem"
git push -u origin main
```
##
### .gitignore | Ignorar pastas ou arquivos
Criar o arquivo .gitignore
```
touch .gitignore
```
<small>Nota: o comando ```touch``` só funciona no terminal Git Bash, o terminal normal não reconhece esse comando.</small>

Adicionar um arquivo ao .gitignore
```
"{nome do arquivo}" >> .gitignore
```

Adicionar uma pasta ao .gitignore
```
echo "{nome da pasta/}" >> .gitignore
```

##
### Criar pasta
```
mkdir {nome da pasta}
```
##
### Criar arquivo README
```
touch README.md ou {nome da pasta}/README.md
```
<small>Nota: o comando ```touch``` só funciona no terminal Git Bash, o terminal normal não reconhece esse comando.</small>

##
### Remover repositorio local
```
rm -r .git/
```
##
### Restaurar última modificação do arquivo
```
git restore nomeDoArquivo
```
##
### Mudar mensagem do commit
```
git commit --amend -m "mensagem"
```
##
### Retornando ao commit anterior
```
git log
git reset --soft codigo do commit
```
##
### Removendo arquivo do commit
```
git reset . ou {nomeDoArquivo}
```
ou
```
git restore --staged {nomeDoArquivo}
```

##
### Puxando alterações do repositório remoto para o repositório local
```
git pull
```

##
### Listar último commit de cada branch
```
git branch -v
```

##
### Listar branches existentes
```
git branch
```

##
### Criar novas branches
```
git branch {nome da nova branch}
```

##
### Criar nova branch e muda para a mesma
```
git checkout -b {nome da nova branch}
```

<small>Nota: Esse comando além de criar uma nova branch, também realiza a troca automatica sem precisar de um novo comando.</small>

##
### Trocar de branch
```
git checkout {nome da branch}
```
##
### Mesclar branches
```
git merge {nome da outra branch}
```
##
### Excluir branch
```
git branch -d {nome da branch}
```
##
### Visualizar diferenças entre branches
``` 
git diff {nome da branch} {nome da outra branch}
```

<small>Exemplo: ```git diff main origin/main```</small>

<small>Visualizando a diferença entre commit da branch local e remota</small>

##
### Clonar branch de um repositório especifico
```
git clone {link do repositório} --branch {nome da branch} --single-branch
```

##
### Comandos para trabalhar com tags
#### lista todas as tags em um repositório
```
git tag
```
#### cria uma nova tag
```
git tag -a {nome da tag} -m "mensagem"
```
#### exclui uma tag
```
git tag -d {nome da tag}
```

##
### Visualizar alterações que serão incluídas no próximo commit
```
git diff --staged
```

##
### Assinatura em um commit
```
git commit -sm "mensagem"
```
Este comando adiciona automaticamente sua assinatura ao commit. A assinatura é um texto que identifica você como o autor do commit e que garante que você concorda com os termos da licença do projeto.

Você também pode usar o comando sem o ```-m``` para criar um commit com uma assinatura, mas sem uma mensagem.
```
git commit -s
```

##
## 🔍 Referências
- [Git - Reference](https://git-scm.com/docs/)
- [Digital Innovation One](https://wwwdio.me/)