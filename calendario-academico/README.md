# Calendário acadêmico · Sprint 2

Trabalho Interdisciplinar · Gustavo Martins de Ávila · Hub de Estudos (Equipe 7)

Tela de **apresentação** (AI): mostra os eventos do calendário lidos do JSON Server. O cadastro dos eventos é a tela da Sprint 1 (pasta `modelo/`).

## Como rodar

Precisa do Node.js. Nesta pasta:

```
npm start
```

Abrir: http://localhost:3000/calendario-academico.html

## Como usar a tela

- **Navegar:** `<` e `>` trocam o mês; **Hoje** volta ao mês atual e seleciona o dia de hoje.
- **Ver um dia:** clique em um dia da grade; a caixa **Eventos do dia** mostra título, matéria, tipo, hora e sala.
- **Filtrar:** por matéria e/ou por tipo; a grade e as duas listas mudam na hora.
- **Próximas entregas:** próximos eventos a partir de hoje, com "hoje", "amanhã" ou "faltam N dias". Clicar leva o calendário até o dia.
- **Legenda:** a cor de cada matéria.

Leitura: `GET /materias` e `GET /eventos?_sort=data,hora&_order=asc,asc`. Eventos da página: `onload`, `onclick` e `onchange`.

Falta: login com permissões por cargo.

A versão oficial está no repositório do grupo (pasta `codigo/public/modulos/calendario/`).
