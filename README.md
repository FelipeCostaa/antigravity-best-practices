# Google Antigravity — Melhores Práticas e Templates de Agentes

Este repositório reúne um guia completo de arquitetura, fluxo de desenvolvimento orientado a especificações (*Spec-Driven Development*) e templates prontos para uso no **Google Antigravity (AGY)**.

## Conteúdo

- **[`guia_melhores_praticas_antigravity.md`](./guia_melhores_praticas_antigravity.md)**: Análise completa com os 5 pilares de customização, fluxo SDD, matriz de permissões e regras do que fazer e não fazer para cada agente.
- **[`AGENTS.md`](./AGENTS.md)**: Modelo enxuto de regras globais do projeto para colocar na raiz de novos repositórios.
- **`.agents/agents/`**: Subagentes especializados prontos para copiar para novos projetos:
  - `architect.md` — Arquiteto de Software & Autor de Especificações (somente leitura).
  - `implementer.md` — Engenheiro de Implementação e testes unitários.
  - `qa-verifier.md` — Engenheiro de QA e verificador adversarial (sem permissão de escrita em código).
  - `security-auditor.md` — Auditor de Segurança AppSec (somente leitura/auditoria).
  - `devops-git.md` — Especialista em integração Git, consolidação de branches/worktrees e CI/CD.

## Como usar em um novo projeto

Copie o arquivo `AGENTS.md` e o diretório `.agents/` para a raiz do seu novo repositório:

```bash
cp AGENTS.md /caminho/do/seu-projeto/
cp -r .agents /caminho/do/seu-projeto/
```

Em seguida, ajuste os comandos oficiais de build, lint e testes no `AGENTS.md` de acordo com a stack do seu projeto.
