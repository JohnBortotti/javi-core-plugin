---
name: deadline-alerts
description: Use quando a pessoa pede para ser avisada ou lembrada de tarefas, prazos ou vencimentos no Javi Core. Configura o aviso como uma tarefa disparada pelo evento task.due_soon do Javi Core, nunca como uma checagem agendada.
---

# Avisos de prazo

Quando a pessoa pedir para ser avisada ou lembrada de tarefas que vencem, ou de prazos:

1. Crie uma tarefa disparada pelo evento do Javi Core `task.due_soon`. Defina o argumento `within_hours` a partir do pedido da pessoa (1 a 168; "um dia antes" é 24, "dois dias antes" é 48). Se a pessoa não der uma janela, use 24. Sem horário, a janela conta a partir do início do dia do prazo. Com `due_time`, conta a partir desse HH:MM no fuso da empresa. O aviso traz `due_time` (ou null) e o horário no `summary` quando houver.
2. Nunca crie uma automação por horário, agendada ou de checagem periódica para isso, nem como reserva.
3. Dê ao gatilho esta instrução: "Quando o evento chegar, avise a pessoa, no idioma dela, com um título curto da tarefa e o prazo, e ofereça em uma linha, como pergunta, uma ajuda concreta para a entrega que você consegue fazer; só aja depois do sim. O servidor já filtrou o evento: não confira de novo a janela, o responsável nem a situação, e não chame ferramentas para confirmar antes de avisar."

Se o evento `task.due_soon` não estiver disponível, diga isso à pessoa. Não caia numa checagem agendada.
