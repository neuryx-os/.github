# Como contribuir com o Neuryx

Obrigado pelo interesse. Este guia vale para todos os repositórios da
organização [`neuryx-os`](https://github.com/neuryx-os), salvo quando um
repositório tiver o próprio `CONTRIBUTING.md`.

## Antes de propor mudanças estruturais

As decisões de arquitetura estão registradas como ADRs em
[`research/adr`](https://github.com/neuryx-os/research/tree/main/adr). Leia os
ADRs relacionados antes de propor uma mudança que afete a composição da
distribuição, o empacotamento ou a relação com o Lyra OS. Para contestar uma
decisão aceita, abra uma issue com o label `tipo: decisão` explicando o que
mudou desde que ela foi tomada.

## Fluxo de trabalho

1. Abra ou escolha uma issue descrevendo o problema ou a proposta.
2. Crie uma branch a partir de `main`.
3. Faça commits pequenos e coesos.
4. Abra um pull request para `main` e preencha o template.
5. Após a revisão, o pull request é integrado por **squash**; a branch é
   apagada automaticamente.

## Mensagens de commit

Usamos [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/),
com a descrição em português e no imperativo do presente do indicativo
(3ª pessoa):

```
<tipo>(<escopo opcional>): <descrição>
```

Tipos mais usados: `feat`, `fix`, `docs`, `chore`, `refactor`, `test`, `ci`,
`build`, `perf`.

Exemplos:

```
feat(model): adiciona verificação de hash SHA-256
fix(gpu): corrige detecção de placas sem nvidia-smi
docs: registra ADR 0008
```

Como os pull requests são integrados por squash, o título do pull request vira
a mensagem do commit final e também deve seguir esse padrão.

## Labels

| Label | Uso |
| --- | --- |
| `tipo: bug` | Algo não funciona |
| `tipo: melhoria` | Nova funcionalidade ou melhoria |
| `tipo: pesquisa` | Investigação técnica |
| `tipo: decisão` | Requer ou registra decisão de arquitetura |
| `tipo: docs` | Documentação |
| `prioridade: alta` | Bloqueia outra entrega |
| `prioridade: normal` | Padrão |
| `status: bloqueado` | Aguarda dependência externa |
| `bom primeiro issue` | Adequado para novos colaboradores |

## Conduta e segurança

Ao participar, você concorda com o [Código de Conduta](CODE_OF_CONDUCT.md).
Vulnerabilidades devem ser reportadas conforme a [política de segurança](SECURITY.md),
nunca por issue pública.
