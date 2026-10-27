# Fichas de Luz v0.3

Aplicativo web responsivo para organizar projetos, fichas de iluminação, biblioteca global de equipamentos e planta 2D / pré-visualização 3D esquemática.

## Publicar no GitHub Pages pelo Android
1. Baixe e extraia o ZIP no celular.
2. Abra o repositório GitHub `fichas-de-luz`.
3. Use **Add file → Upload files** e envie os arquivos que estão diretamente dentro desta pasta (`index.html`, `styles.css`, `app.js`, `manifest.webmanifest`, `sw.js`, `README.md`) para a raiz do repositório.
4. Confirme o commit. O `index.html` deve estar na raiz, não dentro de uma subpasta.
5. Aguarde o GitHub Pages concluir a implantação. Abra o site e atualize sem cache ou acrescente `?v=03` ao endereço.

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
