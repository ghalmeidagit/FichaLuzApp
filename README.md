# Fichas de Luz v0.2

Protótipo web responsivo para planejamento de iluminação cinematográfica.

## Recursos desta versão
- Biblioteca global de equipamentos com cadastro, categorias, busca e sugestões por datalist.
- Planta 2D com zoom, pan, grade, objetos selecionáveis, arrastáveis e legendas.
- Símbolos esquemáticos para luz, câmera, personagem, cadeira, mesa, sofá, parede, janela, bandeira e suporte.
- Cone e cobertura geométrica aproximada de luz, controlados separadamente; luz pode ser desligada.
- Vista isométrica 3D esquemática com os mesmos objetos e coordenadas da planta 2D.
- Fichas com intenção, observações e associação de equipamentos da biblioteca.
- Backup JSON e impressão/exportação via diálogo PDF do navegador.
- Salvamento local no navegador e cache PWA básico.

## Limitações conhecidas
- A vista 3D é uma pré-visualização isométrica leve, não um motor 3D fotorealista nem simulação fotométrica.
- A área de cobertura é geométrica e aproximada; não calcula lux, refletância, difusão física nem exposição.
- Os dados permanecem no armazenamento local deste navegador/aparelho. Ainda não existe sincronização Google Drive nem restauração/importação do JSON pela interface.
- Ao atualizar do MVP v0.1, os dados antigos podem permanecer na chave local antiga, mas não há migração garantida para todas as estruturas anteriores. Exporte um backup antes de substituir a versão publicada.

## Publicação
Envie os arquivos desta pasta para a raiz do repositório GitHub Pages, substituindo os arquivos anteriores. Depois, em Settings > Pages, confirme branch `main` e pasta `/(root)`. Aguarde a publicação e recarregue o site. Para atualizar o PWA instalado, feche e reabra; se persistir versão antiga, limpe o cache do site no Chrome.
