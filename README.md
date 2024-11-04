###Hit the Enemy

Um jogo simples desenvolvido em JavaScript, HTML e CSS, onde o objetivo é acertar o "inimigo" em uma grade de quadrados antes que o tempo acabe ou as vidas se esgotem. O jogador deve clicar no quadrado correto sempre que o inimigo aparece em uma posição aleatória.

Funcionalidades

- **Timer e Pontuação:** O jogo possui um cronômetro de 60 segundos. Cada acerto aumenta a pontuação do jogador.
- **Vidas:** O jogador começa com 3 vidas e perde uma a cada erro.
- **Som de Acerto:** Um som é reproduzido sempre que o jogador acerta a posição do inimigo.
- **Game Over:** O jogo termina quando o tempo ou as vidas se esgotam, mostrando uma mensagem com a pontuação final.

Tecnologias Utilizadas

- **HTML:** estrutura básica do jogo.
- **CSS:** estilos para a interface do jogo.
- **JavaScript:** lógica do jogo, manipulação de DOM, timers e contadores.

Estrutura do Código

`state`

O objeto `state` contém o estado do jogo:

- **view:** Referências aos elementos da interface (quadrados, inimigo, tempo, pontuação, vidas).
- **values:** Variáveis de controle, como o cronômetro, a posição do inimigo, e o número de vidas.
- **actions:** Identificadores dos intervalos de tempo para controle do jogo.

Principais Funções

- **`countDown()`**: Controla o tempo do jogo e verifica se o jogador perdeu por tempo ou por vidas. Exibe uma mensagem de `Game Over` quando o jogo termina.
- **`playSound(audioName)`**: Reproduz um som com base no nome do arquivo de áudio fornecido.
- **`randomSquare()`**: Escolhe um quadrado aleatório para o inimigo aparecer e atualiza a posição correta para o jogador acertar.
- **`addListenerHitbox()`**: Adiciona os ouvintes de clique aos quadrados, verificando se o jogador clicou na posição correta. Incrementa a pontuação em caso de acerto ou diminui as vidas em caso de erro.
- **`init()`**: Inicia o jogo, chamando as funções para definir os intervalos de tempo e os eventos de clique nos quadrados.

Como Jogar

1. Abra o arquivo `index.html` em um navegador.
2. Ao iniciar o jogo, um inimigo aparecerá aleatoriamente em um dos quadrados a cada segundo.
3. Clique no quadrado com o inimigo para aumentar sua pontuação.
4. Cada erro diminui suas vidas em 1. O jogo termina quando o tempo ou as vidas se esgotam.
5. No final, uma mensagem de `Game Over` exibirá sua pontuação final.

Arquivos do Projeto

- **`index.html`**: estrutura HTML do jogo.
- **`style.css`**: estilos para o layout e elementos visuais.
- **`script.js`**: código JavaScript que controla a lógica do jogo.
- **`src/audios/`**: pasta com os sons do jogo (coloque os arquivos de áudio `.m4a` nesta pasta).

Melhorias Futuras

- Adicionar níveis de dificuldade.
- Incluir opção para reiniciar o jogo sem recarregar a página.
- Melhorar os efeitos visuais e sonoros para feedback mais dinâmico.
