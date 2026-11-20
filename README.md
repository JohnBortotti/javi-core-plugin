# Javi Core for Claude

Javi Core is the shared memory of a company: the records of meetings, calls, decisions and e-mails, the tasks that come out of them, and the people, clients, suppliers and projects involved, organized in folders with access per group. This plugin connects Claude to a company's Javi Core and adds the skills that make the conversation work: `/iniciar` opens the day with a briefing, `/resumo` gives the detailed day report, `/registrar` saves what the conversation produced, and the others help with folders, deadlines and reconnecting.

You need a Javi Core account created by your company; the plugin connects to `https://core.javicore.com/mcp` and signs in with OAuth in the browser. Each person sees and changes only what their access allows.

Install in Claude Code:

```
/plugin install javi-core --marketplace JohnBortotti/javi-core-plugin
```

- Documentation: https://javicore.com/ajuda
- Privacy policy: https://javicore.com/privacidade
- Terms: https://javicore.com/termos
- Support: contato@javicore.com
