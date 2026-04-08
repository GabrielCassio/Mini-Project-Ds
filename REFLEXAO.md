## O que foi difícil

**Simular o conflito intencionalmente:** Como já tenho experiência com o Git e o hábito de manter o fluxo de trabalho organizado para evitar problemas de merge, a maior dificuldade foi fazer a engenharia reversa da situação. Forçar o Git a gerar um conflito exigiu sair do modo automático e planejar a arquitetura do erro: criar as branches a partir do mesmo commit base e garantir que ambas alterassem exatamente a mesma linha do mesmo arquivo, forçando o Git a falhar no auto-merge.

## O que ficou claro

**A mecânica interna de comparação do Git:** Ter que provocar o conflito de propósito deixou muito mais evidente como o Git analisa o histórico. Ficou claro na prática como ele usa o ancestral comum para comparar as diferenças nas pontas de cada branch. Entender exatamente quais condições fazem o Git desistir de juntar sozinho reforçou meu entendimento sobre o funcionamento interno da ferramenta, indo além do simples uso dos comandos.

## O que quero explorar (ou o que ainda traz dúvidas)

**Simulação de cenários complexos e *Tree Conflicts*:** Como resolver conflitos comuns de texto já é tranquilo, minha curiosidade agora se volta para situações mais caóticas. Por exemplo: como reproduzir e lidar de forma consistente com tree conflicts (quando uma branch edita um arquivo enquanto a outra o renomeia ou deleta) ou como simular e resolver conflitos em cascata durante um rebase longo com múltiplos commits alterando a mesma estrutura.