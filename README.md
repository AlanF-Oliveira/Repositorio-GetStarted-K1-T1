# Comandos Git

## Configuração inicial
```bash
git init                          # inicia um repositório
git remote add origin <url>       # conecta ao repositório remoto
git clone <url>                   # clona um repositório existente
```

## Fluxo básico
```bash
git status                        # ver estado dos arquivos
git add .                         # adiciona tudo pra staging
git commit -m "mensagem"          # cria um commit
git push -u origin main           # envia pro remoto (primeira vez)
git push                          # envia pro remoto
git pull                          # baixa e mescla mudanças do remoto
git fetch                         # baixa mudanças sem mesclar
```

## Branches
```bash
git branch                        # lista branches
git branch -M main                # renomeia branch atual pra main
git switch nome-branch             # troca de branch
git switch -c nome-branch          # cria e já troca pra nova branch
git merge nome-branch              # mescla branch na atual
```

## Histórico
```bash
git log                           # histórico completo
git log --oneline                 # histórico resumido
git log --oneline --all --graph   # histórico de todas as branches, com gráfico
git reflog                        # histórico de movimentações do HEAD
```

## Desfazendo coisas
```bash
git revert <hash>                 # desfaz um commit criando outro commit (seguro em branch compartilhada)
git reset --soft <hash>           # volta HEAD, mantém staging e arquivos
git reset --mixed <hash>          # volta HEAD e staging, mantém arquivos
git reset --hard <hash>           # volta HEAD, staging e arquivos (destrutivo)
git checkout -- arquivo           # descarta mudanças não commitadas de um arquivo
```

## Outros úteis
```bash
git stash                         # guarda mudanças não commitadas temporariamente
git stash pop                     # traz de volta o que foi guardado
git cherry-pick <hash>            # aplica um commit específico na branch atual
git rebase main                   # reaplica commits da branch atual sobre a main
git tag nome-tag                  # cria uma tag
```