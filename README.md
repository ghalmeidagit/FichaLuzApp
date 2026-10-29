# Fichas de Luz v0.26 — fichas v1.1 + exemplo real

Aplicativo local-first para planejamento de iluminação cinematográfica, com planta 2D cotada, vista 3D orbitável, biblioteca de equipamentos, cinco fichas operacionais revisadas e exportação em PDF.

## O que mudou na v0.26
- Substituição dos campos específicos pelas cinco fichas revisadas na versão editorial v1.1.
- Ficha 1: intenção dramática, beats, blocking com tolerâncias, cobertura e invariantes.
- Ficha 2: geometria, aberturas, estudo solar, superfícies, energia, som e riscos.
- Ficha 3: geometria de cada fonte (centro, alvo, distância, ângulos), alvos/leituras, câmeras, modificadores, plano B e histórico.
- Ficha 4: pergunta, hipóteses, variável/controles, resultados, critérios prévios e limites da aprovação.
- Ficha 5: registro por plano, desvios, incidentes, concessões, continuidade, pós e fechamento.
- Inclui backup JSON demonstrativo do plano de filmagem “Quando Você Não Está na Sala” (V7, diária 29/10/2026), organizado em cinco blocos operacionais, com cinco fichas por bloco.

## Como abrir o exemplo
1. Abra o app e exporte **Backup JSON** dos projetos atuais.
2. Clique em **Restaurar backup** e selecione `EXEMPLO_PLANO_FILMAGEM_v1_1.json`.
3. Atenção: restaurar substitui os dados locais atuais. O backup anterior é essencial.
4. Selecione o projeto demonstrativo e navegue pelas cenas.
5. A exportação PDF documenta a cena ativa; exporte cada cena separadamente.

## Importante sobre os dados de exemplo
- A/B/C e ações/movimentos vêm do plano de filmagem V7.
- Lentes da A e B são preliminares no próprio plano; lente da C permanece a confirmar.
- O plano não contém leituras de luz, posições medidas, valores de exposição, dados elétricos ou kit de iluminação confirmado. Esses campos permanecem pendentes ou como alvo/hipótese.
- A referência de estúdio 4,40 × 3,30 m e grid 3,50 m vem de contexto de planejamento anterior e está marcada como **a confirmar para esta locação**. A planta é esquemática [S], não um desenho aprovado.
- A fonte principal e a fonte de fundo na planta são propostas de ensaio, não equipamentos confirmados para a diária.
- A vista 3D é esquemática, não simulação física/fotométrica.

## Atualização segura
1. Faça backup JSON antes de atualizar.
2. Substitua os arquivos do app pelo conteúdo deste ZIP mantendo `icons/` na raiz.
3. Não limpe os dados do navegador; a chave local foi preservada para manter projetos existentes.
4. Teste um projeto antigo e o projeto de demonstração após publicar.

## Testes
Execute a partir da raiz com Node.js:
```bash
node --check app.js
node --check sw.js
node QA_TESTS/test_migration.cjs
node QA_TESTS/test_sw.cjs
node QA_TESTS/test_room_drawing.cjs
node QA_TESTS/test_outside_objects.cjs
node QA_TESTS/test_pdf_diagrams.cjs
node QA_TESTS/test_five_forms.cjs
node QA_TESTS/test_multiscene_3d.cjs\nnode QA_TESTS/test_v1_1_forms.cjs\nnode QA_TESTS/test_demo_project.cjs
```
