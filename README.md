# Go Calendar

## Integrantes

- Pedro Pourchet
- Bruno Toshiaki

---

## O que é este projeto?

O **Go Calendar** é um sistema de lembretes por e-mail.

O usuário se cadastra no site, entra no painel, escolhe uma data, um horário e escreve uma mensagem. No dia e horário escolhido, o sistema envia um e-mail para ele com o lembrete.

Exemplo de uso: "Me lembra no dia 20/06 às 08h que tenho consulta médica."

---

## Objetivo

Criar um sistema web simples onde qualquer pessoa possa cadastrar lembretes e recebê-los automaticamente por e-mail na data escolhida.

---

## Tecnologias que serão usadas

- **PHP** — linguagem principal do sistema
- **MySQL** — banco de dados (guarda usuários e lembretes)
- **HTML e CSS** — telas do sistema (cadastro, painel, formulários)
- **PHPMailer** — biblioteca para enviar os e-mails

---

## Estado atual do projeto

> Em planejamento — 1º bimestre

Neste momento, o repositório está sendo organizado e o planejamento está sendo feito. O sistema ainda não foi desenvolvido.

---

## Documentos do projeto

- [Visão geral do projeto](docs/planejamento/visao-do-projeto.md)
- [Backlog (lista de funcionalidades)](docs/planejamento/backlog.md)
- [Roadmap (cronograma de versões)](docs/planejamento/roadmap.md)
- [Organização da equipe](docs/fluxo-de-trabalho/organizacao-da-equipe.md)
- [Kanban (quadro de tarefas)](docs/fluxo-de-trabalho/kanban.md)
- [Gantt (cronograma visual)](docs/fluxo-de-trabalho/gantt.md)
- [Desenvolvimento vs Produção](docs/fluxo-de-trabalho/desenvolvimento-vs-producao.md)

---

## Estrutura de pastas do repositório

```
README.md
src/
docs/
docs/planejamento/
docs/planejamento/visao-do-projeto.md
docs/planejamento/backlog.md
docs/planejamento/roadmap.md
docs/fluxo-de-trabalho/
docs/fluxo-de-trabalho/desenvolvimento-vs-producao.md
docs/fluxo-de-trabalho/organizacao-da-equipe.md
docs/fluxo-de-trabalho/kanban.md
docs/fluxo-de-trabalho/gantt.md
docs/evidencias/
docs/evidencias/controle-de-versao/
```

---

## Como o projeto vai funcionar (resumo)

1. O usuário acessa o site e se cadastra com nome, e-mail e senha.
2. Faz login e entra no painel.
3. Clica em "Novo lembrete", escolhe a data, o horário e escreve a mensagem.
4. O sistema salva o lembrete no banco de dados.
5. No dia e horário certo, o sistema envia um e-mail automático para o usuário.