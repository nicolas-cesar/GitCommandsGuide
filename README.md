# GitCommandsGuide
# Atividade em conjunto com o time de desenvolvimento

# *Git e Github* (Instruções e Configurações)
As aulas nos permitiram aprender sobre as ferramentas utilizadas para o desenvolvimento de trabalhos em equipe

## git status
**Descrição:** O comando *git status* é utilizado para mostrar o estado atual do repositório, incluindo quais arquivos foram modificados, quais estão prontos para realizar o comando *git commit*, e quais não estão rastreados.
**Exemplo Prático:**
```git status``` - mostra o estado atual do repositório 

## git add
**Descrição:** O comando *git add* é utilizado para adicionar arquivos que foram modificados ao índice staging area para que possam ser incluídos no próximo commit.
**Exemplo Prático:**
```git add <nome-do-arquivo>``` - Adiciona o arquivo *nome-do-arquivo* na staging area
```git add .``` - Adiciona todos os arquivos modificados para a staging area
```git add *<.extensão>``` - Adiciona todos os arquivos com a extensão *.extensão* para a staging area

# git commit
O comando *git commit* é usado no Git para salvar as alterações realizadas no código em um repositório. Cada "commit" é uma espécie de registro ou ponto de restauração que armazena o estado do projeto naquele momento, juntamente com uma mensagem descritiva ou genérica sobre o que foi alterado. Esse processo é fundamental para o controle de versão, pois permite acompanhar o histórico de alterações e, se necessário, reverter o código para um estado anterior.

# Git push
o *git push* serve para enviar as alterações commitadas no repositório local para o repositório remoto.

# Git stash
o *git stash* possibilita guardar temporariamente as alterações realizadas na branch local, de forma a reaplicar essas alterações em outras branches locais.
