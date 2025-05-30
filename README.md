# 📚 API de Cadastro de Professores e Disciplinas

Este projeto expõe uma API REST para gerenciar professores, disciplinas e o relacionamento entre eles.

## ▶️ Execução

Certifique-se de que o backend está rodando localmente na porta `3000`.

## 🔐 Informações Sensíveis

Os exemplos abaixo utilizam dados fictícios ou anonimizados para proteção de informações pessoais como CPF e e-mail.

## 📦 Endpoints

### ➕ Criar Professor

**POST /professor**

Headers:  
Content-Type: application/json

Body:
```json
{
  "nome": "Henrique Louro",
  "email": "henrique.louro@fatec.sp.gov.br",
  "cpf": "07494812857"
}
```

Respostas comuns:
- ✅ 200: Professor cadastrado com sucesso  
- ❌ 400: CPF ou e-mail já em uso / CPF inválido / E-mail inválido

### 📋 Listar Professores

**GET /professor**

Resposta:
```json
[
  {
    "_id": "6838fa1318bc4405f1a662e5",
    "nome": "Henrique Louro",
    "email": "henrique.louro@fatec.sp.gov.br",
    "cpf": "07494812857"
  },
  {
    "_id": "6838fa5918bc4405f1a662e7",
    "nome": "Roberto Lima",
    "email": "carlos.silva@fatec.sp.gov.br",
    "cpf": "63479695051"
  }
]
```

### ✏️ Atualizar Professor

**PUT /professor**

Headers:  
Content-Type: application/json

Body:
```json
{
  "id": "6838fa6d18bc4405f1a662e9",
  "nome": "Juliana Mendes",
  "email": "odetinha.roitman@fatec.sp.gov.br",
  "cpf": "32082128016"
}
```

### ❌ Remover Professor

**DELETE /professor**

Headers:  
Content-Type: application/json

Body:
```json
{
  "id": "6838fa6d18bc4405f1a662e9"
}
```

## 📚 Disciplinas

### ➕ Criar Disciplina

**POST /disciplina**

Headers:  
Content-Type: application/json

Body:
```json
{
  "descricao": "Técnicas de Programação II"
}
```

e

```json
{
  "descricao": "Lógica de Programação"
}
```

### 📋 Listar Disciplinas

**GET /disciplina**

Resposta:
```json
[
  {
    "_id": "6838fbf418bc4405f1a662f4",
    "descricao": "Técnicas de Programação II"
  },
  {
    "_id": "6838fc0d18bc4405f1a662f6",
    "descricao": "Lógica de Programação"
  }
]
```

## 🔗 Relacionamento Professor–Disciplina

### ➕ Associar Professor a Disciplina

**POST /professor_has_disciplina**

Headers:  
Content-Type: application/json

Body:
```json
{
  "professor": "6838fa1318bc4405f1a662e5",
  "disciplina": "6838fbf418bc4405f1a662f4"
}
```

e

```json
{
  "professor": "6838fa5918bc4405f1a662e7",
  "disciplina": "6838fc0d18bc4405f1a662f6"
}
```
