# GitCommandsGuide
# Atividade em conjunto com o time de desenvolvimento

# *Git e Github* (Instruções e Configurações)
As aulas nos permitiram aprender sobre as ferramentas utilizadas para o desenvolvimento de trabalhos em equipe

# git status
O *git status* mostra o estado atual do repositório, incluindo quais arquivos foram modificados, quais estão prontos para commit, e quais não estão rastreados.

## git add
**Descrição:** Este comando atualiza o índice usando o conteúdo atual encontrado na árvore de trabalho, para preparar o conteúdo marcado para o próximo commit. 
Normalmente, ele adiciona o conteúdo atual de caminhos existentes como um todo, mas com algumas opções, também pode ser usado para adicionar conteúdo com apenas parte das mudanças feitas aos arquivos da árvore de trabalho aplicadas, ou remover caminhos que não existem mais na árvore de trabalho. Este comando pode ser executado várias vezes antes de um *commit*. Ele adiciona apenas o conteúdo dos arquivos especificados no momento em que o comando *add* é executado; 
se você quiser que alterações subsequentes sejam incluídas no próximo commit, você deve executar *git add* novamente para adicionar o novo conteúdo ao índice. 
**Exemplo Prático:**    
```git add --sparse``` Permite a atualização de entradas do índice fora do cone de checkout esparso. Normalmente, o git add se recusa a atualizar entradas do índice cujos caminhos não se encaixam no cone de checkout esparso, pois esses arquivos podem ser removidos da árvore de trabalho sem aviso. Consulte git-sparse-checkout[1] para mais detalhes.

```git add --interactive``` Adicione conteúdos modificados na árvore de trabalho de forma interativa ao índice. Argumentos de caminho opcionais podem ser fornecidos para limitar a operação a um subconjunto da árvore de trabalho. Consulte "Modo interativo" para detalhes.

## git commit
**Descrição:** Cria um novo commit contendo o conteúdo atual do índice e a mensagem de log fornecida descrevendo as alterações. O novo commit é um filho direto do HEAD, geralmente a ponta do branch atual, e o branch é atualizado para apontar para ele (a menos que nenhum branch esteja associado à árvore de trabalho, caso em que o HEAD está "desanexado", conforme descrito em git-checkout[1]).
O conteúdo a ser commitado pode ser especificado de várias maneiras:
- usando `git-add[1]` para "adicionar" incrementos de mudanças ao índice antes de usar o comando commit (Nota: até mesmo arquivos modificados devem ser "adicionados");
- usando `git-rm[1]` para remover arquivos da árvore de trabalho e do índice, novamente antes de usar o comando commit;
- listando arquivos como argumentos do comando commit (sem os switches `--interactive` ou `--patch`), caso em que o commit ignorará as mudanças já preparadas no índice e, em vez disso, registrará o conteúdo atual dos arquivos listados (que já devem ser conhecidos pelo Git);
- usando o switch `-a` com o comando commit para "adicionar" automaticamente mudanças de todos os arquivos conhecidos (ou seja, todos os arquivos que já estão listados no índice) e "remover" automaticamente arquivos no índice que foram removidos da árvore de trabalho, e então realizar o commit;
- usando os switches `--interactive` ou `--patch` com o comando commit para decidir, um a um, quais arquivos ou partes devem fazer parte do commit além do conteúdo no índice, antes de finalizar a operação. Consulte a seção "Modo Interativo" de `git-add[1]` para aprender a operar nesses modos.

**Exemplo Prático:**  
```git commit --all``` Informa ao comando para preparar automaticamente arquivos que foram modificados e deletados, mas novos arquivos que você não informou ao Git não serão afetados.
 
```git commit --short``` Ao fazer uma execução simulada, forneça a saída no formato curto. Consulte git-status[1] para detalhes. Implica --dry-run.

# Git push
o *git push* serve para enviar as alterações commitadas no repositório local para o repositório remoto.

# Git stash
o *git stash* possibilita guardar temporariamente as alterações realizadas na branch local, de forma a reaplicar essas alterações em outras branches locais.
