# Fichas de Luz v0.6

Aplicativo web responsivo para organizar projetos, fichas de iluminação, biblioteca global de equipamentos e planta 2D / pré-visualização 3D esquemática.

## Publicar no GitHub Pages pelo Android
1. Baixe e extraia o ZIP no celular.
2. Abra o repositório GitHub `fichas-de-luz`.
3. Use **Add file → Upload files** e envie os arquivos que estão diretamente dentro desta pasta (`index.html`, `styles.css`, `app.js`, `manifest.webmanifest`, `sw.js`, `README.md`) para a raiz do repositório.
4. Confirme o commit. O `index.html` deve estar na raiz, não dentro de uma subpasta.
5. Aguarde o GitHub Pages concluir a implantação. Abra o site e atualize sem cache ou acrescente `?v=06` ao endereço.

## Dados e segurança
- Projetos e equipamentos ficam no armazenamento local do navegador neste dispositivo.
- O backup JSON exporta projetos e biblioteca; Restaurar backup importa um JSON compatível e substitui os dados locais após confirmação.
- Não há sincronização com Google Drive nesta versão.
- Faça backup antes de limpar dados do navegador, trocar de aparelho ou atualizar se houver dados importantes.

## Recursos
- Página inicial com criar, abrir, editar, duplicar e excluir projetos.
- Salvamento automático local.
- Fichas técnicas por projeto, duplicação e exclusão.
- Biblioteca global com busca, categorias, cadastro, edição e exclusão.
- Planta 2D com zoom, pan, objetos arrastáveis, legendas e fachos estimados.
- Vista isométrica 3D esquemática usando os mesmos objetos.
- Exportação por impressão / PDF do navegador.

## Limitações conhecidas
- A vista 3D é esquemática, não um render fisicamente realista.
- A cobertura de luz é geométrica aproximada, não uma medição fotométrica.
- A sincronização entre dispositivos e com Google Drive não está implementada.


## Correções v0.6
- Dez fichas iniciais seguem os títulos e a lógica de Fichas 01–10 resumidas do Volume 2.
- Busca de equipamentos com sugestões customizadas durante a digitação, compatível com telas móveis.
- Rotação direta no desenho 2D: selecione um objeto e arraste o manipulador circular que aparece ligado a ele.
- As sugestões são selecionáveis por toque; o equipamento é associado ao cadastro global existente.


## Exportação PDF v0.6
A exportação agora abre um relatório próprio para impressão, com capa do projeto, planta capturada sem os controles do aplicativo, legenda/posições, fichas preenchidas e apenas equipamentos associados ao projeto. No diálogo de impressão do Android/Chrome, escolha “Salvar como PDF”.


## Atualização v0.6
- Mantém a chave de armazenamento local existente para preservar projetos de teste.
- Estrutura específica para cada uma das dez fichas, alinhada ao documento Fichas_01-10_Iluminacao_Cinematografica.
- Autocomplete customizado para equipamento na planta, com resultados priorizados por correspondência de início de nome/palavra.
- Controles de rotação direta ampliados e botões de ajuste fino de 15 graus.
- PDF com planta 2D limpa gerada separadamente da interface e inclusão dos campos específicos de cada ficha.
- O render 3D continua esquemático e não é simulação fotométrica.
