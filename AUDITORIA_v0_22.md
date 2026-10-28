# Auditoria v0.22 — correções da revisão v0.21

## Correções aplicadas
- Atualizados nome do manifesto, cabeçalho/rodapé e cache para v0.22.
- Atualizada a instrução de atualização sem cache para `?v=022`.
- Adicionados marcadores vermelhos “FORA DO ESTÚDIO” para objetos cujas coordenadas X/Y ultrapassam o perímetro configurado, tanto na planta 2D quanto na vista isométrica. Os objetos não são deslocados automaticamente.
- Mantida a representação do fundo como área no piso com largura × comprimento.

## Limites
- A vista 3D continua sendo uma projeção isométrica em Canvas, não uma cena 3D orbital.
- Os testes de código não substituem inspeção visual em Android/navegador real nem conferência de PDF exportado.
- Objetos fora do perímetro são destacados na tela; a lista de coordenadas no PDF ainda deve ser conferida pelo usuário.
