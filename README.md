# Gantt Heaven

Editor de diagramas de Gantt em um único arquivo HTML — sem instalação, sem servidor.

## Como usar

Abra `index.html` no navegador (duplo clique). O programa sempre abre com um projeto vazio — use 📂 Abrir ou 🕘 Recentes para continuar um projeto (o da última sessão também volta com ↶ Desfazer). Clique em **?** para ver a ajuda.

- **Mover tarefa:** arraste a barra.
- **Alterar início/fim:** arraste a borda esquerda/direita da barra.
- **Dependências:** arraste a bolinha à direita de uma barra até outra tarefa (ou linha da lista). A tarefa dependente só começa após o fim da anterior e é empurrada automaticamente. Clique numa seta para removê-la. Ciclos são bloqueados.
- **Categorias:** coluna Categoria na tabela (edite direto por ela) e botão 🏷️ Categorias — cada categoria tem uma cor, exibida como borda da cápsula da tarefa (e faixa colorida na lista). Escolha a categoria no duplo clique da tarefa; clique numa categoria da legenda para destacá-la.
- **Membros do time:** botão 👥 Membros — cada membro tem uma cor; a barra da tarefa assume a cor do(s) responsável(is). Clique num membro da legenda para destacar as tarefas dele.
- **Editar detalhes:** duplo clique na barra/linha (nome, datas, duração, progresso, membros, dependências, notas).
- **Salvar:** salvamento automático no navegador + `Ctrl+S` grava um arquivo `.ganttheaven` (`Ctrl+O` abre; também é possível arrastar o arquivo para a janela). Arquivos `.json` antigos continuam abrindo.
- **Colunas:** em ▦ Colunas escolha Dias, Semanas ou Meses para agrupar/sombrear as colunas. Clique no cabeçalho para destacar aquele dia, semana ou mês (clique de novo para remover).
- **Recentes:** botão 🕘 Recentes reabre os últimos 10 projetos abertos/salvos (o próprio arquivo, quando o navegador permite acesso a arquivos; senão, a cópia guardada no navegador).
- **PDF:** botão 🖨️ PDF (`Ctrl+P`): escolha o período (de/até ou atalhos como "Este mês"), se mostra os períodos destacados e se inclui a tabela (e quais colunas). Depois "Salvar como PDF".
- **CSV:** botão 📑 CSV exporta para planilha as tarefas de um período (de/até ou atalhos), com escolha de colunas (inclui extras: progresso, dependências, notas) e separador.
- **Atalhos:** `Ctrl+Z`/`Ctrl+Y` desfazer/refazer, `Insert` nova tarefa, `Delete` excluir, `Enter` editar, `Ctrl` + roda do mouse = zoom.

## Finanças (aba 💰)

- **Planilha Orçamentária:** registre previsões de gastos e receitas (nome, categoria, quantia total e previsão por mês). Edite os valores direto nas células, como numa planilha; a coluna Diferença avisa se a distribuição mensal não fecha com a quantia. Totais por categoria, saldo previsto do mês e acumulado.
- **Histórico de Pagamento:** transações em ordem cronológica, cada uma ligada a um item da planilha, com tipo (saída por padrão / entrada), destinatário (nome, telefone, e-mail, chave Pix), contrato, observação, **Nota Fiscal** e **Comprovante** (PDF, PNG, JPG ou JPEG). Configure uma vez a 📁 Pasta dos documentos (caminho + seleção da pasta) e o caminho completo dos arquivos escolhidos dessa pasta é preenchido automaticamente.
- **Desembolso:** previsto × realizado por item e por mês, com % pago e barras de progresso.
- Cada sub-aba tem exportação 🖨️ PDF e 📑 CSV com escolha de período (e de colunas, no histórico).

As durações são em dias corridos (fins de semana aparecem sombreados).
