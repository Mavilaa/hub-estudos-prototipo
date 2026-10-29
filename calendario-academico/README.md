# Calendário acadêmico · Sprint 2 (em andamento)

Trabalho Interdisciplinar · Gustavo Martins de Ávila · Hub de Estudos (Equipe 7)

Tela de **apresentação** (AI): mostra os eventos do calendário lidos do JSON Server. O cadastro dos eventos é a tela da Sprint 1 (pasta `modelo/`).

## Como rodar

Precisa do Node.js. Nesta pasta:

```
npm start
```

Abrir: http://localhost:3000/calendario-academico.html

## Feito até agora

- **Grade do mês** montada por JavaScript (DOM), cada evento na cor da matéria; dias passados ficam apagados.
- **Navegação:** `<` e `>` trocam o mês; **Hoje** volta ao mês atual e seleciona o dia de hoje.
- **Legenda** com a cor de cada matéria.
- **Próximas entregas:** próximos eventos a partir de hoje, com "hoje", "amanhã" ou "faltam N dias". Clicar leva o calendário até o dia.

Leitura: `GET /materias` e `GET /eventos?_sort=data,hora&_order=asc,asc`.

Falta: filtros por matéria e por tipo, eventos do dia selecionado e login com permissões por cargo.
