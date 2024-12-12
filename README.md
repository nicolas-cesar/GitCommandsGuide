# GitCommandsGuide
# Atividade em conjunto com o time de desenvolvimento

# *Git e Github* (Instruções e Configurações)
As aulas nos permitiram aprender sobre as ferramentas utilizadas para o desenvolvimento de trabalhos em equipe

# git status
O *git status* mostra o estado atual do repositório, incluindo quais arquivos foram modificados, quais estão prontos para commit, e quais não estão rastreados.

## git add
**Descrição:** Este comando atualiza o índice usando o conteúdo atual encontrado na árvore de trabalho, para preparar o conteúdo marcado para o próximo commit. 
Normalmente, ele adiciona o conteúdo atual de caminhos existentes como um todo, mas com algumas opções, também pode ser usado para adicionar conteúdo com apenas 
parte das mudanças feitas aos arquivos da árvore de trabalho aplicadas, ou remover caminhos que não existem mais na árvore de trabalho.
Este comando pode ser executado várias vezes antes de um *commit*. Ele adiciona apenas o conteúdo dos arquivos especificados no momento em que o comando *add* é executado; 
se você quiser que alterações subsequentes sejam incluídas no próximo commit, você deve executar *git add* novamente para adicionar o novo conteúdo ao índice.
**Exemplo Prático:**    
```git add --sparse``` Permite a atualização de entradas do índice fora do cone de checkout esparso. Normalmente, o git add se recusa a atualizar entradas do índice 
cujos caminhos não se encaixam no cone de checkout esparso, pois esses arquivos podem ser removidos da árvore de trabalho sem aviso. Consulte git-sparse-checkout[1] 
para mais detalhes.

```git add --interactive``` Adicione conteúdos modificados na árvore de trabalho de forma interativa ao índice. Argumentos de caminho opcionais podem ser fornecidos 
para limitar a operação a um subconjunto da árvore de trabalho. Consulte "Modo interativo" para detalhes.

## git commit
O comando *git commit* é usado no Git para salvar as alterações realizadas no código em um repositório. Cada "commit" é uma espécie de registro ou ponto de restauração que armazena o estado do projeto naquele momento, juntamente com uma mensagem descritiva ou genérica sobre o que foi alterado. Esse processo é fundamental para o controle de versão, pois permite acompanhar o histórico de alterações e, se necessário, reverter o código para um estado anterior.

# Git push
o *git push* serve para enviar as alterações commitadas no repositório local para o repositório remoto.

# Git stash
o *git stash* possibilita guardar temporariamente as alterações realizadas na branch local, de forma a reaplicar essas alterações em outras branches locais.