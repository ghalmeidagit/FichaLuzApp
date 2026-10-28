# Auditoria v0.21 — visão 3D e dimensões do fundo

## Alterações
- A visão 3D foi redesenhada como uma projeção isométrica de Canvas 2D: piso, paredes translúcidas, arestas verticais e grade métrica opcional.
- O fundo branco agora é tratado como uma área retangular no piso com largura e comprimento, não como altura.
- A posição do fundo segue a parede escolhida e sua extensão para dentro do estúdio.
- Os fachos na vista 3D são volumes esquemáticos projetados da posição Z da fonte para o piso; não representam fotometria real.
- Os objetos são desenhados com as coordenadas X/Y/Z existentes. Na vista 3D, objetos podem ser selecionados; a edição espacial continua disponível pelos campos e pela planta 2D.
- A leitura de `backdropHeight` foi mantida como compatibilidade para projetos antigos; o novo campo é `backdropLength`.
- Validação impede que largura ou comprimento do fundo exceda a dimensão disponível da sala na parede escolhida.
- A planta 2D e o PDF mostram a área do fundo como retângulo cotado, com largura × comprimento.
- Cache e identificação de versão atualizados para v0.21.

## Verificações executadas
- `node --check app.js`: aprovado.
- `node --check sw.js`: aprovado.
- `node QA_TESTS/test_migration.cjs`: 19 asserções aprovadas.
- `node QA_TESTS/test_sw.cjs`: 5 verificações aprovadas.
- `node QA_TESTS/test_room_drawing.cjs`: testes estáticos de planta aprovados após atualização.

## Limitações
- A vista 3D é uma projeção isométrica em Canvas, não uma cena WebGL com câmera orbital nem renderização fisicamente baseada.
- Não foi possível executar um teste visual real no Android nesta sessão. Recomenda-se confirmar enquadramento, legibilidade e posições no aparelho antes de substituir a versão publicada.
- A altura do estúdio permanece opcional; quando ausente, a vista usa 3,50 m como altura esquemática e indica que é estimada.
- Verificações adicionais de compatibilidade do campo legado e da terminologia do PDF: 2 aprovadas.
