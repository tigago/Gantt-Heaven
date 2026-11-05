# Gantt Heaven

Editor de diagramas de Gantt em um único arquivo HTML — sem instalação, sem servidor.

## Como usar

Abra `index.html` no Chrome ou Edge (duplo clique). Clique em **?** na barra de ferramentas para ver a ajuda.

- **Mover tarefa:** arraste a barra.
- **Alterar início/fim:** arraste a borda esquerda/direita da barra.
- **Dependências:** arraste a bolinha à direita de uma barra até outra tarefa (ou linha da lista). A tarefa dependente só começa após o fim da anterior e é empurrada automaticamente. Clique numa seta para removê-la. Ciclos são bloqueados.
- **Membros do time:** botão 👥 Membros — cada membro tem uma cor; a barra da tarefa assume a cor do(s) responsável(is). Clique num membro da legenda para destacar as tarefas dele.
- **Editar detalhes:** duplo clique na barra/linha (nome, datas, duração, progresso, membros, dependências, notas).
- **Salvar:** salvamento automático no navegador + `Ctrl+S` grava um arquivo `.gantt.json` (`Ctrl+O` abre; também é possível arrastar o arquivo para a janela).
- **Atalhos:** `Ctrl+Z`/`Ctrl+Y` desfazer/refazer, `Insert` nova tarefa, `Delete` excluir, `Enter` editar, `Ctrl` + roda do mouse = zoom.

As durações são em dias corridos (fins de semana aparecem sombreados).
