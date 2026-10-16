# Hub de Estudos - Cadastro de eventos do calendário

Trabalho Interdisciplinar - Sprint 1 (Cadastro de Informações / CRUD)
Aluno: Gustavo Martins

Tela de calendário onde o aluno cadastra, vê, altera e exclui eventos da faculdade
(provas, trabalhos, tarefas, quizzes e aulões). Os dados ficam no JSON Server (`db.json`)
e aparecem no calendário do mês, com filtro por matéria.

## Como rodar

Precisa ter o Node.js instalado.

1. Abrir o terminal dentro desta pasta
2. Instalar o JSON Server (só na primeira vez):

```
npm install
```

3. Iniciar o servidor:

```
npm start
```

4. Abrir no navegador: http://localhost:3000/

   A página inicial carrega o calendário completo, incluindo HTML, CSS e JavaScript.
   Também é possível acessar diretamente: http://localhost:3000/calendario.html

Para voltar aos dados iniciais: parar o servidor (Ctrl+C), rodar `npm run reset` e depois `npm start` de novo.

## Operações

| Operação | Como fazer na tela | Requisição |
|---|---|---|
| Ver (READ) | Abrir a página e clicar em um dia do calendário | GET /eventos |
| Cadastrar (CREATE) | Preencher o formulário "Novo evento" e clicar em Salvar evento | POST /eventos |
| Alterar (UPDATE) | Clicar em Editar no evento, mudar os dados e clicar em Salvar alterações | PUT /eventos/:id |
| Excluir (DELETE) | Clicar em Excluir no evento e confirmar | DELETE /eventos/:id |

## Estrutura de dados (db.json)

```json
{
  "materias": [
    { "id": 1, "sigla": "AEDS2", "nome": "Algoritmos e Estruturas de Dados II", "cor": "#2b5fc4" }
  ],
  "eventos": [
    {
      "id": 9,
      "titulo": "Prova 2",
      "materia": "CALC2",
      "tipo": "prova",
      "data": "2026-10-22",
      "hora": "08:50",
      "sala": "310"
    }
  ]
}
```

- `tipo`: prova, trabalho, tarefa, quiz ou aulao
- `hora` vazia = evento de dia inteiro
- `sala` é opcional

## Arquivos

```
calendario.html          página
assets/css/styles.css    estilos (inclui a versão para celular)
assets/js/app.js         código JavaScript
db.json                  dados do JSON Server
db.inicial.json          cópia dos dados iniciais (npm run reset)
package.json             dependência do json-server
```
