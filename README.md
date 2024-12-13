# GitCommandsGuide
# Atividade em conjunto com o time de desenvolvimento

# *Git e Github* (Instruções e Configurações)
As aulas nos permitiram aprender sobre as ferramentas utilizadas para o desenvolvimento de trabalhos em equipe

# git status
O *git status* mostra o estado atual do repositório, incluindo quais arquivos foram modificados, quais estão prontos para commit, e quais não estão rastreados.

# git add
O *git add* adiciona mudanças de arquivos ao índice staging area para serem incluídas no próximo commit.

# git commit
O comando *git commit* é usado no Git para salvar as alterações realizadas no código em um repositório. Cada "commit" é uma espécie de registro ou ponto de restauração que armazena o estado do projeto naquele momento, juntamente com uma mensagem descritiva ou genérica sobre o que foi alterado. Esse processo é fundamental para o controle de versão, pois permite acompanhar o histórico de alterações e, se necessário, reverter o código para um estado anterior.

## git push
**Descrição:** O comando *git push* é usado para enviar as alterações commitadas no repositório local para o repositório remoto. Ele sincroniza o histórico de commits do local para o remoto, tornando as atualizações disponíveis para outros colaboradores. Se não for especificado o nome do repositório remoto (como origin), o Git utiliza o repositório remoto padrão configurado para o branch atual. Caso não haja especificação de origin ou o nome do repositório remoto, o Git usará as configurações definidas pelo comando git remote add e git branch --set-upstream-to. Isso pode simplificar o fluxo de trabalho em projetos onde o repositório remoto padrão já foi configurado.
**Exemplo Prático:**
```git push``` - *Envia as alterações do branch atual para o repositório remoto padrão configurado*
```git push origin main``` - *Envia as alterações do branch atual para o branch correspondente no repositório remoto*  
```git push origin nome-da-branch``` - *Envia para um branch específico no repositório remoto* 

## git stash
**Descrição:** O comando *git stash* permite salvar temporariamente alterações não commitadas no repositório local, limpando a área de trabalho sem perder o progresso. As alterações salvas podem ser reaplicadas posteriormente na mesma ou em outra branch.
**Exemplo Prático:**
```git stash```  - *Guarda as alterações atuais*  
```git stash list``` - *Lista os stashes salvos*
```git stash pop``` - *Reaplica e remove o stash da lista*  
```git stash apply```  - *Reaplica o último stash*