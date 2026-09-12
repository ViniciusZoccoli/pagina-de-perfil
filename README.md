# Página de Perfil

Projeto da Prova Individual 13 — CMP2304 C02 / Tecnologia de Construção de Software I — PUC Goiás.

Aplicação web simples de página de perfil, desenvolvida para demonstrar o ciclo completo
de desenvolvimento com Git, GitHub e GitFlow.

## Autor

Vinicius Zoccoli de Moraes Barros

## Tecnologias

HTML5 e CSS3.

## Estrutura de branches (GitFlow)

| Branch | Finalidade |
|---|---|
| `main` | Código em produção. Recebe merges de release e hotfix, sempre com tag de versão. |
| `develop` | Linha de integração contínua do desenvolvimento. |
| `feature/informacoes-perfil` | Implementação de nome, foto e descrição do perfil. |
| `release/1.0.0` | Preparação da versão 1.0.0, com inclusão do campo profissão. |
| `hotfix/1.0.1-corrige-titulo` | Correção do título da página após a publicação da 1.0.0. |

## Histórico do ciclo de desenvolvimento

1. **Commit inicial** — criação do repositório e do README.
2. **Versão mínima** — estrutura base da página em HTML e CSS na `develop`.
3. **Feature** — branch `feature/informacoes-perfil` criada a partir da `develop`, com dois commits:
   adição de foto e nome, e adição da seção de descrição.
4. **Integração** — merge da feature na `develop` com `--no-ff`, preservando a ramificação no histórico.
5. **Release 1.0.0** — branch `release/1.0.0` criada a partir da `develop`, com commit de inclusão
   do campo profissão. Finalizada com merge em `main` e `develop` e tag `1.0.0`.
6. **Hotfix** — erro identificado em produção após a 1.0.0: título da página incorreto.
   Branch `hotfix/1.0.1-corrige-titulo` criada a partir da `main`, com commit exclusivo da correção.
7. **Versão corrigida** — hotfix integrado em `main` e `develop`, com tag `1.0.1`.

## Versões

| Tag | Descrição |
|---|---|
| `1.0.0` | Página de perfil com nome, foto, descrição e profissão. |
| `1.0.1` | Correção do título da página. |

## Observação sobre o fluxo

O GitFlow foi aplicado manualmente por meio de comandos Git nativos, mantendo a nomenclatura
padrão de branches (`feature/`, `release/`, `hotfix/`) e utilizando `merge --no-ff` em todas as
integrações, de modo a preservar a ramificação no histórico.