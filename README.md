# 🎮 Jogo da Forca em Python (Versão Melhorada)

Versão evoluída do tradicional **Jogo da Forca** desenvolvido em Python para o terminal. A partir de uma estrutura base criada em aula, o código recebeu melhorias significativas em organização de dados, experiência do usuário (UX) e mecânicas de pontuação.

---

## 🚀 O que mudou? (Melhorias e Evolução)

O código original possuía uma lista única e estática de palavras focada apenas em tecnologia. Abaixo estão listadas as atualizações implementadas nesta nova versão:

### 1. Separação de Palavras por Temas
* **Antes:** Uma lista simples (`palavras = [...]`) com termos genéricos de computação.
* **Agora:** Criação de um dicionário (`temas`) que organiza o vocabulário por categorias específicas: **Tecnologia**, **Jogos** e **Escola**.

### 2. Menu de Seleção de Temas Interativo
* **Antes:** O jogo sorteava qualquer palavra de forma totalmente aleatória na inicialização.
* **Agora:** A função `escolher_palavra()` exibe uma interface gráfica textual listando as categorias disponíveis e solicita que o usuário escolha seu tema de preferência antes de começar.

### 3. Validação e Tratamento de Erros
* **Antes:** Se o usuário digitasse algo inválido no início, o programa poderia quebrar ou se comportar de forma inesperada.
* **Agora:** Caso o jogador digite um tema inválido ou inexistente, o sistema ativa um mecanismo de segurança que seleciona o tema padrão (*"tecnologia"*) automaticamente, permitindo que o jogo continue sem interrupções.

### 4. Ajuste no Sistema de Pontuação e Novo Bônus
* O equilíbrio de pontos por jogada foi reajustado para tornar o jogo mais dinâmico:
  * **Acerto:** +5 pontos.
  * **Erro:** -3 pontos.
* **Bônus de Vitória Perfeita:** Adicionada uma nova regra que verifica se o jogador venceu a partida sem perder nenhuma vida (`vidas == 6`). Caso consiga esse feito, ele é recompensado com **+50 pontos adicionais**.

### 5. Loop de Jogo ("Jogar Novamente")
* **Antes:** O jogo executava uma única vez. Se o usuário quisesse jogar de novo, precisava reiniciar o script manualmente no terminal.
* **Agora:** Toda a execução foi encapsulada dentro de uma estrutura de repetição (`while True`). Ao final de cada partida (vitória ou derrota), o terminal pergunta se o jogador quer jogar novamente, encerrando o programa de forma elegante somente se a resposta for diferente de "s".
