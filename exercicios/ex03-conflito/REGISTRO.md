### O que causou o conflito (qual arquivo, qual trecho)

O conflito aconteceu porque o Git encontrou alterações nas mesmas linhas em duas branches diferentes (`main` e `docs/atualiza-readme`). Isso afetou dois arquivos:

* **No `REFLEXAO.md`:** Houve uma colisão no título da última seção. Uma branch tinha a versão com o texto `## O que quero explorar (ou o que ainda traz dúvidas)`, enquanto a outra tentava inserir `## O que quero explorar (ou o que ainda é confuso)`.
* **No `README.md`:** O Git esbarrou na inserção de toda a nova estrutura do documento (título do projeto, descrição das pastas e passos para execução) colidindo com o conteúdo que já estava lá.

### Como decidi qual versão manter

Usando o VS Code, eu analisei os blocos de código que o Git marcou com `<<<<<<<`, `=======` e `>>>>>>>`. 

* Para o **`REFLEXAO.md`**, achei que a frase "ou o que ainda é confuso" combinava melhor com o que eu queria passar, então escolhi manter essa versão.
* Para o **`README.md`**, decidi aceitar a versão mais longa (a alteração que adicionava as 30 linhas de Markdown), pois ela continha toda a documentação completa do miniprojeto. Apenas apaguei o conteúdo excedente e os marcadores de conflito.

### O comando ou ação usada para marcar o conflito como resolvido

Como eu fiz a resolução direto pelo VS Code, o fluxo foi o seguinte:

1. Editei os arquivos manualmente, escolhendo o código final e apagando as marcações do Git.
2. Salvei os arquivos e, no terminal, usei os comandos `git add README.md` e `git add REFLEXAO.md` (poderia ter usado o `git add .`) para sinalizar ao Git que os conflitos estavam resolvidos.
3. Por fim, rodei o comando `git commit` para concluir o merge e fechar o ciclo da resolução, seguido de um `git push` para mandar as alterações para o GitHub.