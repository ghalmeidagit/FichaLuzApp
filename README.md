# Fichas de Luz v0.24.1

Aplicativo local-first para planejamento de iluminação cinematográfica, com planta 2D cotada, vista isométrica esquemática, biblioteca de equipamentos, cinco fichas operacionais e exportação em PDF.

## As cinco fichas
1. Cena e intenção
2. Locação e condições
3. Folha de luz e planta
4. Teste e aprovação
5. Execução e relatório do dia

Cada ficha inclui autor, versão, estado temporal, tipo do documento (esquema/estimado/medido) e distribuição. Os campos específicos têm orientações curtas para favorecer preenchimento objetivo no set.

## Atualização segura
1. No app atual, exporte **Backup JSON** antes de substituir os arquivos.
2. Atualize os arquivos do repositório pelo conteúdo deste ZIP, mantendo a pasta `icons/` na raiz.
3. Não limpe os dados do navegador. A chave local foi preservada e a migração converte as seis fichas anteriores para a nova estrutura de cinco, arquivando os registros legados e preservando conteúdo sem mapeamento em observações ou fichas adicionais.
4. Após publicar, abra o aplicativo e confira um projeto antigo antes de continuar editando.

## Planta e vista 3D
A planta usa coordenadas X/Y em metros, com origem no centro do estúdio. Objetos fora do perímetro são sinalizados e não são movidos automaticamente. A vista isométrica 3D é esquemática; os fachos não representam fotometria real.

## Testes
Execute com Node.js, a partir da raiz:

```bash
node --check app.js
node --check sw.js
node QA_TESTS/test_migration.cjs
node QA_TESTS/test_sw.cjs
node QA_TESTS/test_room_drawing.cjs
node QA_TESTS/test_outside_objects.cjs
node QA_TESTS/test_pdf_diagrams.cjs
node QA_TESTS/test_five_forms.cjs
```

Consulte `AUDITORIA_v0_24.md` para o escopo de auditoria e as limitações da validação.
