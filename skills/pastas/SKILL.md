---
name: pastas
description: Use quando a pessoa pede para ver, abrir ou mostrar as pastas, a árvore de documentos ou os arquivos da empresa no navegador, ou digita /pastas. Abre a página Pastas do Javi Core no navegador do computador.
---

# Pastas

Abra a árvore de documentos no navegador, para a pessoa ver as pastas, os registros e os arquivos.

1. Se ainda não souber a empresa, chame `quem_sou`. O id da empresa é `company.id`. Se `company` vier null e `companies` listar mais de uma, chame `usar_empresa` com o id de uma delas e chame `quem_sou` de novo.
2. A origem é a do servidor MCP, sem `/mcp` no fim. Monte `https://origem/admin/empresas/{company.id}/pastas`. Se a pessoa nomear uma pasta que `listar_pasta` já devolveu, acrescente o id dela: `https://origem/admin/empresas/{company.id}/pastas/{id}`.
3. Abra essa URL no navegador do aplicativo (o navegador embutido do Codex ou do Claude Code). Se esse navegador não existir, mostre o link em uma linha.
4. Diga em uma linha, em português, que a árvore de pastas está aberta. A pessoa vê só o que já pode ver. Não mude quem vê uma pasta por este caminho: se um proprietário ou admin pedir, use `definir_acesso_pasta_grupo` (e `listar_grupos` para ver os grupos de cada pasta) aqui no chat.

Não invente o id da empresa. Se `quem_sou` não trouxer a empresa e `usar_empresa` não resolver, diga isso e não abra um endereço incompleto.
