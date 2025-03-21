# Guia Rápido de Git

## 1. Clonar um repositório existente
Se você deseja obter uma cópia local de um repositório já existente no GitHub:

```sh
git clone https://github.com/GarciaGGOO/api_bmt_by_IA.git
```
Esse comando cria uma cópia do repositório na máquina local.

## 2. Inicializar um repositório Git localmente
Se você ainda não inicializou o repositório Git no diretório atual:

```sh
git init
```
Isso criará um repositório Git local.

## 3. Adicionar um repositório remoto
Se o repositório ainda não estiver vinculado ao GitHub:

```sh
git remote add origin https://github.com/GarciaGGOO/NomeDoRepositório 
```

## 4. Verificar o status do repositório
Para ver quais arquivos foram modificados e quais estão pendentes de commit:

```sh
git status
```

## 5. Adicionar arquivos ao repositório
```sh
git add .
```

## 6. Fazer o commit com uma mensagem descritiva
```sh
git commit -m "descrição"
```

## 7. Enviar alterações para o GitHub
```sh
git push -u origin main
```

---

# Trabalhando com branches

## 1. Criar e mudar para uma nova branch
```sh
git checkout -b nome-da-branch
```

## 2. Listar todas as branches existentes
```sh
git branch -a
```

## 3. Renomear uma branch local
```sh
git branch -m novo-nome-da-branch
```

## 4. Excluir uma branch local
```sh
git branch -d nome-da-branch
```

Se a branch ainda não estiver mesclada e quiser forçar a remoção:
```sh
git branch -D nome-da-branch
```

## 5. Excluir uma branch remota
```sh
git push origin --delete nome-da-branch
```

## 6. Atualizar o repositório local com alterações remotas
```sh
git pull origin main
```

## 7. Reverter um commit sem excluir as alterações
```sh
git reset --soft HEAD~1
```

## 8. Desfazer todas as alterações locais e voltar ao último commit
```sh
git reset --hard HEAD
```

## 9. Reverter um commit específico criando um novo commit
```sh
git revert <commit-hash>
```

## 10. Verificar os commits realizados
```sh
git log --oneline --graph --decorate --all
```

## 11. Criar uma tag em um commit (para versões específicas)
```sh
git tag -a v1.0 -m "Versão 1.0"
git push origin v1.0
```

## 12. Configurar um repositório para lembrar as credenciais do usuário
```sh
git config --global credential.helper store
```
Isso salva as credenciais para evitar precisar digitá-las a cada `push`.
