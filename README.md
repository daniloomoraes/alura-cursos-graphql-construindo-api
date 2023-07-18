node 18

npm install

npm start

em outra aba do terminal rodar: npx json-server --watch api/data/dados.json

Exemplo Consultando lista:

query {
  users {
    nome
    role {
      type
    }
  }
}

Exemplo Consulta especifica:

query {
  user(id: 1) {
    nome
  }
}

Exemplo adicionar registro:

mutation {
  adicionaUser(
    user: {
      nome: "teste",
      ativo: true,
      email: "teste@teste.com",
      role: ESTUDANTE,
      createdAt: "2022-07-18"
    }
  ){
    nome
  }
}

Exemplo atualiza registro:

mutation {
  atualizaUser (
    id: 10,
    user: {
			nome: "teste",
      ativo: true,
      email: "teste@teste.com",
      role: ESTUDANTE,
      createdAt: "2022-07-18"
    }
  ){
    mensagem
  }
}

Exemplo deleta registro:

mutation {
  deletaUser (
    id: 10
  ){
    mensagem
  }
}
