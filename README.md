# API Professores e Disciplinas

API para gerenciar professores, disciplinas e associações.

## Como usar

Servidor rodando na porta 3000. Use JSON nas requisições.

## Endpoints e exemplos de uso com curl

**Cadastrar professor**  
curl -X POST http://localhost:3000/professor -H "Content-Type: application/json" -d "{"nome":"Henrique Louro","email":"henrique.louro@fatec.sp.gov.br","cpf":"07494812857"}"

markdown
Copiar
Editar

**Listar professores**  
curl -X GET http://localhost:3000/professor

markdown
Copiar
Editar

**Atualizar professor**  
curl -X PUT http://localhost:3000/professor -H "Content-Type: application/json" -d "{"id":"ID_DO_PROFESSOR","nome":"Juliana Mendes","email":"juliana.mendes@fatec.sp.gov.br","cpf":"32082128016"}"

markdown
Copiar
Editar

**Excluir professor**  
curl -X DELETE http://localhost:3000/professor -H "Content-Type: application/json" -d "{"id":"ID_DO_PROFESSOR"}"

markdown
Copiar
Editar

**Cadastrar disciplina**  
curl -X POST http://localhost:3000/disciplina -H "Content-Type: application/json" -d "{"descricao":"Técnicas de Programação II"}"

markdown
Copiar
Editar

**Listar disciplinas**  
curl -X GET http://localhost:3000/disciplina

markdown
Copiar
Editar

**Associar professor e disciplina**  
curl -X POST http://localhost:3000/professor_has_disciplina -H "Content-Type: application/json" -d "{"professor":"ID_DO_PROFESSOR","disciplina":"ID_DA_DISCIPLINA"}"

bash
Copiar
Editar

## Observação

Projeto feito por aluno do 3º semestre da FATEC.
