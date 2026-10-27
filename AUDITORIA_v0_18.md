# Auditoria técnica — Fichas de Luz v0.18

## Correções desta revisão
- Corrigido o caminho de `sw.js` no teste automatizado: agora o teste funciona diretamente dentro de `QA_TESTS/`.
- Adicionado `QA_TESTS/test_migration.cjs`, que executa as funções reais de migração extraídas de `app.js` em VM isolada e testa consolidação de dez fichas, arquivo legado, status, notas, idempotência, fichas extras/desconhecidas e conflitos de campos.
- Manifesto inclui ícones PNG de 192 e 512 px; ambos são adicionados ao cache de instalação.
- Atualizados os identificadores da versão para v0.18 e o parâmetro de cache do README.

## Testes executados
- `node --check app.js`: aprovado.
- `node --check sw.js`: aprovado.
- `node --check QA_TESTS/test_sw.cjs`: aprovado.
- `node --check QA_TESTS/test_migration.cjs`: aprovado.
- `node QA_TESTS/test_sw.cjs`: 5 verificações aprovadas.
- `node QA_TESTS/test_migration.cjs`: 10 asserções aprovadas.
- `python -m json.tool manifest.webmanifest`: aprovado.
- ZIP testado com `unzip -t`.

## Limitações
Testes em VM e dados sintéticos não substituem a validação no navegador real. Ainda é necessário testar em Android: atualização do service worker, uso offline após uma primeira abertura online, rotação e cobertura do facho, restauração de backup real e exportação PDF. Não é correto declarar ausência absoluta de erros sem essas provas.
