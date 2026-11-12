# Gantt Heaven

Editor de diagramas de Gantt em um único arquivo HTML — sem instalação, sem servidor.

## 🎬 Tutorial em vídeo

Veja em menos de 3 minutos como usar o cronograma e a aba de finanças: [video/tutorial-gantt-heaven.mp4](video/tutorial-gantt-heaven.mp4) (narrado em português).

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
- **Numeração das semanas:** em № Semanas escolha **ISO** (padrão), **desde o começo do ano** (a semana de 1º de janeiro é a S1), **desde uma data** (a semana que contém a data escolhida é a S1; antes dela as semanas ficam sem número) ou **reiniciar a cada mês** (a semana que contém o dia 1º é a S1 daquele mês: S1/mar, S2/mar…). As semanas vão de segunda a domingo. A escolha fica salva no projeto e aparece no cabeçalho do cronograma, no PDF (que informa a numeração usada) e na coluna opcional **Semanas** da tabela do PDF e do CSV.
- **Recentes:** botão 🕘 Recentes reabre os últimos 10 projetos abertos/salvos (o próprio arquivo, quando o navegador permite acesso a arquivos; senão, a cópia guardada no navegador).
- **PDF:** botão 🖨️ PDF (`Ctrl+P`): escolha o período (de/até ou atalhos como "Este mês"), se mostra os períodos destacados, se usa o nível de zoom da visualização (a largura dos dias como está na tela) e se inclui a tabela (e quais colunas). Depois "Salvar como PDF".
- **CSV:** botão 📑 CSV exporta para planilha as tarefas de um período (de/até ou atalhos), com escolha de colunas (inclui extras: progresso, dependências, notas) e separador.
- **Atalhos:** `Ctrl+Z`/`Ctrl+Y` desfazer/refazer, `Insert` nova tarefa, `Delete` excluir, `Enter` editar, `Ctrl` + roda do mouse = zoom.

## Finanças (aba 💰)

A aba Finanças controla o dinheiro do projeto em três sub-abas, que conversam entre si: a **Planilha Orçamentária** diz quanto se pretende gastar e receber, o **Histórico de Pagamento** registra o que de fato entrou e saiu, e o **Desembolso** compara as duas coisas mês a mês. O 🔍 controle deslizante (ou `Ctrl` + roda do mouse) ajusta o zoom das tabelas.

### 📋 Planilha Orçamentária

- **+ Gasto** / **+ Receita** abrem o diálogo do item: nome, categoria (sugere as já usadas), **Quantidade**, **Unidade** (cachê, mensal, diária, hora…), **Qtd. de unidade** e **Valor unitário**. O **Total** é calculado sozinho (quantidade × qtd. de unidade × valor unitário), mas pode ser digitado diretamente.
- Os itens ficam agrupados em Receitas e Gastos e, dentro deles, por categoria, com subtotais. Para renomear uma categoria, edite-a na própria linha de total.
- Os valores de um item só mudam pelo diálogo (botão ✎ na linha); ✕ exclui.
- No topo aparecem o total de **Receitas**, de **Gastos** e o **Saldo** previsto.
- A coluna **Distribuído** mostra quanto do total já foi distribuído pelos meses (no Desembolso) e a **Diferença** avisa quando a distribuição não fecha com o total.

### 🧾 Histórico de Pagamento

- **+ Transação** registra uma **saída** (padrão) ou **entrada**: data, valor, item da planilha a que pertence e destinatário/origem. O diálogo mostra quanto estava previsto para aquele item no mês e quanto já foi pago.
- **👤 Destinatários:** cadastro de nome, telefone, e-mail e chave Pix, reutilizado em todas as transações.
- **＋ Novo pagamento** (em cada saída) abre uma nova transação já com valor, item, destinatário e contrato copiados, ideal para pagamentos recorrentes. **Salvar e nova** mantém o diálogo aberto para lançar outra.
- **Anexos:** cada transação guarda **Nota Fiscal**, **Comprovante** e **Contrato** (PDF, PNG, JPG ou JPEG), anexados pelo diálogo ou direto na tabela ("+ anexar"); 👁 abre o arquivo.
- **📁 Pasta dos documentos:** configure uma vez o caminho completo da pasta onde ficam as notas e comprovantes e selecione-a; a partir daí, o caminho completo de cada arquivo escolhido dessa pasta é preenchido automaticamente (🔄 atualiza a lista de arquivos). A lista é guardada separadamente para cada projeto.
- **🗂️ Anexos (ZIP):** baixa um ZIP com as notas, comprovantes e contratos das transações de um período (o navegador pede autorização para ler a pasta, se preciso).
- **Filtros** por mês, item (serviço), destinatário e tipo (entradas/saídas); ✖ Filtros limpa todos. Os totais de saídas, entradas e saldo acompanham o filtro.
- A coluna **Saldo acumulado** mostra o caixa após cada transação; a **Observação** pode ser editada direto na tabela.

### 📊 Desembolso

- Uma linha por item e uma coluna por mês (escolha o período em "Meses de … até …"; alterne entre ↓ Gastos e ↑ Receitas).
- Em cada célula, digite o valor **previsto** para o mês; acima dele aparecem o **realizado** (soma do histórico) e o **% pago**, com uma barrinha colorida (parcial, 100% pago, acima do previsto, não previsto no mês).
- **⚖ Distribuir** (ao passar o mouse no nome do item) divide uma quantia igualmente entre os meses escolhidos; **Limpar previsão** apaga a distribuição.
- **🔎 Histórico** (ao passar o mouse numa célula ou no item) abre o Histórico de Pagamento já filtrado por aquele item e mês.
- O nome de cada item mostra o % que ele representa do orçamento; as linhas de categoria e de total somam tudo, e o rodapé traz o **saldo acumulado real** (pelo histórico) e o **saldo previsto acumulado**.

### Exportação

- Cada sub-aba tem 🖨️ **PDF** e 📑 **CSV**, com escolha de período (e de colunas e saldo acumulado, no histórico).

As durações são em dias corridos (fins de semana aparecem sombreados).
