# O Porquinho Guloso

Jogo feito em HTML, CSS e JavaScript, sem bibliotecas nem imagens externas. Todos os desenhos e sons são criados pelo próprio código.

## Como publicar no GitHub Pages

1. Criar uma conta em https://github.com (se ainda não houver).
2. Carregar em **New repository**, dar o nome `porquinho-guloso` e escolher **Public**.
3. Carregar em **uploading an existing file** e arrastar o `index.html` (e este `README.md`).
4. Carregar em **Commit changes**.
5. Ir a **Settings → Pages**. Em *Branch*, escolher `main` e a pasta `/ (root)`. Carregar em **Save**.
6. Ao fim de 1 ou 2 minutos, o jogo fica disponível em:
   `https://<nome-de-utilizador>.github.io/porquinho-guloso/`

## Ideias para a apresentação

- **Ciclo de jogo:** cerca de 60 vezes por segundo, o programa lê os comandos, actualiza as posições e desenha tudo outra vez (função `ciclo`).
- **Colisões:** cada objecto é um círculo. Se a distância entre dois centros for menor do que a soma dos raios, tocaram-se (função `distancia`).
- **Estados do jogo:** `menu`, `a jogar`, `pausa` e `fim`.
- **Dificuldade:** a cada 10 pontos sobe-se de nível; aparecem mais lobos e mais poças de lama, e os lobos ficam mais rápidos.
- **Desenhos com código:** o porco, o lobo, as maçãs e a trufa são feitos com círculos, elipses e triângulos no `canvas`.
- **Personalização:** cada jogador escolhe a cor (9 cores ou qualquer outra no selector), um de 8 chapéus e um nome. A escolha fica guardada no navegador (`localStorage`), por isso mantém-se da próxima vez.
- **Uma função, dois sítios:** a mesma função `desenharFiguraPorco` desenha o porco no jogo e na pré-visualização; só muda o "pincel" que recebe.
- **Sons sem ficheiros:** usam a *Web Audio API* para gerar tons.

## Coisas fáceis de alterar (para experimentar)

| O quê | Onde no código |
|---|---|
| Velocidade do porco | `velocidade: 230` |
| Pontos para subir de nível | `Math.floor(pontos / 10)` |
| Número de vidas | `vidas = 3` |
| Cores disponíveis | lista `CORES` |
| Novo chapéu | acrescentar à lista `CHAPEUS` e um `case` em `desenharChapeu` |
| Duração da trufa | `vida: 6` |
