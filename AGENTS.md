# Regras do Projeto (AGENTS.md)

## Comandos Oficiais
- Build: `npm run build`
- Testes Unitários: `npm test -- <caminho-do-arquivo>`
- Typecheck: `npm run typecheck`
- Linter: `npm run lint`

## Padrões de Arquitetura e Código
- Linguagem: TypeScript estrito (`strict: true`). Proibido usar `any`.
- Validação de entrada: Use sempre schemas `zod` na camada de controller.
- Acesso a dados: Nunca escreva SQL manual fora de `src/repositories/`.

## Restrições de Segurança para Agentes
- Nunca leia, imprima ou modifique arquivos `.env*`.
- Nunca adicione novas dependências ao `package.json` sem aprovação prévia do usuário.
- Sempre execute o typecheck e os testes unitários do módulo alterado antes de concluir uma tarefa.
