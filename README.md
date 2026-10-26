# Fichas de Luz — MVP v0.1

Protótipo web responsivo em português para organizar projetos de iluminação cinematográfica.

## Já implementado
- Projetos com cliente, data, locação e intenção visual.
- Dez fichas com campos editáveis e status.
- Planta esquemática superior com fontes, pessoas e câmeras; mover por arrasto e editar dados dos elementos.
- Inventário inicial editável baseado no kit informado.
- Registro de testes e avaliação final.
- Backup JSON exportável e relatório imprimível/salvável em PDF pelo navegador.
- Persistência local; service worker para shell offline quando servido por HTTPS ou localhost.

## Limitação importante: Google Drive
A sincronização automática com Drive **não está conectada nesta versão**. Ela exige OAuth 2.0/Google Cloud ou uma camada Apps Script, permissões, e uma estratégia para conflitos entre celular e computador. O conector Drive do ChatGPT não está disponível para conexão nesta sessão. Por enquanto, o botão Backup JSON exporta um arquivo que pode ser guardado manualmente no Drive. Importação/restauração e sincronização são próximas etapas; não trate dois backups como se estivessem sincronizados.

## Executar no computador
Entre na pasta e execute `python3 -m http.server 8080`; abra `http://localhost:8080`. Para instalar como PWA em dispositivos móveis, publique os arquivos em hospedagem HTTPS estática. A publicação não foi feita.

## Próxima iteração
1. Importar/restaurar backup JSON com validação.
2. Conectar Google Drive e resolver conflitos entre dispositivos.
3. Incluir a imagem da planta no PDF, escala/legenda mais rigorosas e ferramentas de direção da luz.
