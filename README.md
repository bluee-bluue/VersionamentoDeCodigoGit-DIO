# Curso Versionamento de Código com Git e GitHub da DIO

Comandos do Git ensinados no curso Versionamento de Código com Git e GitHub da [Digital Innovation One](https://wwwdio.me/).

## 📚 Documentação
- [Documentação Git](https://git-scm.com/doc)
- [Documentação GitHub](https://docs.github.com/)

## 💻 Comandos das aulas

| Ação | Como usar |
|-------|---------|
| Definir/Alterar email | [Como usar](#definiralterar-email) |
| Definir/Alterar nome | [Como usar](#definiralterar-nome) |
| Novo repositório | [Como usar](#inicialização-de-um-novo-repositório-git) |
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
| Trocar de branch | [Como usar](#trocar-de-branch) |
| Mesclar branches | [Como usar](#mesclar-branches) |
| Excluir branch | [Como usar](#excluir-branch) |
| Visualizar diferenças entre branches | [Como usar](#visualizar-diferenças-entre-branches) |
| Clonar branch de um repositório especifico | [Como usar](#clonar-branch-de-um-repositório-especifico) |

### Definir/Alterar email
```
git config --global user.email {email}
```

### Definir/Alterar nome
```
git config --global user.nome {nome}
```

### Inicialização de um novo repositório Git
```
git init
git add . ou {nome do arquivo}
git commit -m "mensagem"
git branch -m main
git remote add origin {link do repositório}
git push -u origin main
```

<small>Nota: git branch -m main deve ser usado apenas quando você deseja renomear de 'master' para 'main'.</small>

### Remover pasta ou arquivo do controle de versão
```
git rm -r --cached {nome da pasta}
```
ou
```
git rm --cached {nome do arquivo}
```

### Atualizar commit
```
git add . ou {nome do arquivo}
git commit -m "mensagem"
git push -u origin main
```

### .gitignore | Ignorar pastas ou arquivos
```
echo "pasta/" ou "arquivo" >> .gitignore
```

### Criar pasta
```
mkdir {nome da pasta}
```

### Criar arquivo README
```
touch README.md ou {nome da pasta}/README.md
```

### Remover repositorio local
```
rm -rf .git
```

### Restaurar última modificação do arquivo
```
git restore nomeDoArquivo
```

### Mudar mensagem do commit
```
git commit --amend -m "mensagem"
```

### Retornando ao commit anterior
```
git log
git reset --soft codigo do commit
```

### Removendo arquivo do commit
```
git reset nomeDoArquivo
```

```
git restore --staged nomeDoArquivo
```

### Puxando alterações do repositório remoto para o repositório local
```
git pull
```

### Listar último commit de cada branch
```
git branch -v
```

### Listar branches existentes
```
git branch
```

### Criar novas branches
```
git checkout -b {nome da nova branch}
```

### Trocar de branch
```
git checkout {nome da branch}
```

### Mesclar branches
```
git merge {nome da outra branch}
```

### Excluir branch
```
git branch -d {nome da branch}
```

### Visualizar diferenças entre branches
``` 
git diff {nome da branch} {nome da outra branch}
```

<small>Exemplo: ```git diff main origin/main```</small>

<small>Visualizando a diferença entre commit da branch local e remota</small>

### Clonar branch de um repositório especifico
```
git clone {link do repositório} --branch {nome da branch} --single-branch
```

## 🔍 Referências
- [Digital Innovation One](https://wwwdio.me/).