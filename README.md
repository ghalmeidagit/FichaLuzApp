# Fichas de Luz v0.18 — seis etapas

Aplicativo web responsivo para organizar projetos de iluminação, biblioteca de equipamentos e planta 2D / pré-visualização 3D esquemática.

## Publicar no GitHub Pages pelo Android
1. Faça backup JSON no aplicativo antes de atualizar.
2. Extraia este ZIP.
3. No repositório GitHub `fichas-de-luz`, envie os arquivos desta pasta para a raiz e confirme o commit.
4. Aguarde a implantação do GitHub Pages e abra o site. Se a versão antiga continuar aparecendo, atualize sem cache ou abra o endereço com `?v=018`.

## Fichas reorganizadas
1. Cena e intenção
2. Locação e condições
3. Estratégia de luz
4. Planta e posições
5. Equipamento e verificação
6. Execução e ajustes

A estrutura foi reduzida de dez etapas para seis fichas, agrupando campos relacionados e mantendo campos específicos por etapa. A migração consolida a estrutura conhecida de dez fichas antigas nos seis cartões e preserva cópia integral em `legacyFichas`. Fichas com tipo desconhecido não são classificadas pela posição: ficam marcadas como fichas legadas/adicionais, mantendo seus dados para revisão manual. Os seis tipos principais ausentes são acrescentados sem reclassificar os cartões existentes. Faça backup antes de atualizar.

## Dados e segurança
- Projetos e equipamentos ficam no armazenamento local do navegador neste dispositivo.
- O backup JSON exporta projetos e biblioteca; restaurar um backup substitui os dados locais após confirmação.
- Não há sincronização automática com Google Drive.
- Faça backup antes de limpar dados do navegador, trocar de aparelho ou atualizar.

## Recursos e limitações
- Projetos: criar, abrir, editar, duplicar e excluir.
- Salvamento automático local.
- Fichas técnicas por projeto, biblioteca global de equipamentos e exportação para impressão/PDF.
- Planta 2D com zoom, pan, objetos arrastáveis, rotação e fachos estimados.
- Vista isométrica 3D esquemática; não é render fisicamente realista.
- A cobertura de luz é geométrica aproximada, não medição fotométrica.
- A sincronização entre dispositivos e com Google Drive não está implementada.


## Revisão técnica v0.18

Correções desta versão:
- Identificador estável para cada tipo de ficha; a renderização e o PDF deixam de depender apenas da posição da ficha.
- Migração sem perda intencional: cópia integral das fichas de origem em `legacyFichas`; status preservado quando há correspondência; campos sem destino ficam nas observações ou no registro legado.
- Fichas desconhecidas não recebem um tipo com base na posição da lista.
- Formulários reduzidos a metadados compartilhados, campos específicos da etapa, equipamentos e observações; os campos técnicos aparecem na etapa pertinente.
- Restaurar backup executa a migração e normalização antes de salvar.
- Projetos com outras quantidades de fichas são preservados; fichas extras são marcadas como adicionais, sem receber campos específicos de uma etapa por engano.
- Unificação da convenção angular do facho entre planta interativa e PDF, incluindo a inversão vertical necessária ao canvas do PDF.
- Eixo central tracejado com seta na cobertura de luz, na planta e no PDF.
- Enquadramento do PDF passa a considerar o alcance máximo das fontes ligadas.
- Alça de rotação acompanha a orientação do objeto.
- Correção da versão no cabeçalho e atualização do cache PWA.

## Limites da validação

A sintaxe de `app.js` foi validada com `node --check`, e foram executados testes de migração com dados sintéticos para projeto de dez fichas, contagem não padrão, tipo desconhecido e preservação de status/campos. A validação visual de navegador/Android e impressão PDF precisa ser feita no dispositivo de publicação; não é declarada como concluída. Não publique por cima da versão ativa sem backup JSON.


## Testes automatizados v0.18
Execute com Node.js a partir da raiz do pacote:

```sh
node QA_TESTS/test_sw.cjs
node QA_TESTS/test_migration.cjs
```

Os testes usam dados sintéticos e verificam o service worker e os caminhos principais da migração. Eles não substituem testes visuais no dispositivo real.
