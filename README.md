# RocketNotes API

Uma API RESTful para gerenciar notas pessoais.

## Descrição

RocketNotes é uma aplicação web que permite aos usuários criar, editar, excluir e pesquisar notas pessoais. A API fornece os endpoints para realizar essas operações, usando o formato JSON para enviar e receber os dados. A API usa o SQLite como banco de dados, e o Express como framework web.

Este projeto é o backend da aplicação RocketNotes, um web app que permite aos usuários criar e gerenciar notas pessoais de forma simples e intuitiva. O frontend da aplicação está hospedado no Netlify, e o código fonte está disponível no GitHub: https://rocketnotes-makeyournotes.netlify.app/ https://github.com/HomerMau/RocketNotes


## Instalação

Para instalar e executar a API localmente, você precisa ter o Node.js e o NPM instalados no seu computador. Em seguida, siga estes passos:

1. Clone o repositório do GitHub usando o comando `git clone https://github.com/HomerMau/API.git`.
2. Navegue até a pasta do projeto usando o comando `cd API`.
3. Instale as dependências do projeto usando o comando `npm install`.
4. Inicie o servidor usando o comando `npm start`.
5. A API estará disponível no endereço `http://localhost:3000`.

## Uso

A API possui os seguintes endpoints:

- `GET /notes`: retorna todas as notas existentes no banco de dados.
- `GET /notes/:id`: retorna a nota com o id especificado.
- `POST /notes`: cria uma nova nota com os dados enviados no corpo da requisição.
- `PUT /notes/:id`: atualiza a nota com o id especificado com os dados enviados no corpo da requisição.
- `DELETE /notes/:id`: exclui a nota com o id especificado.
- `GET /notes/search?query`: retorna as notas que contêm a palavra-chave especificada na query.

Aqui está um exemplo de como usar o endpoint `POST /notes` para criar uma nova nota:

```json
// Requisição
POST http://localhost:3000/notes
Content-Type: application/json

{
  "title": "Minha primeira nota",
  "content": "Esta é uma nota de teste criada pela API."
}

// Resposta
{
  "success": true,
  "message": "Nota criada com sucesso.",
  "data": {
    "_id": "60c9a7f8f9b6f41a8c8c0f6d",
    "title": "Minha primeira nota",
    "content": "Esta é uma nota de teste criada pela API.",
    "createdAt": "2024-02-28T14:59:04.123Z",
    "updatedAt": "2024-02-28T14:59:04.123Z"
  }
}
```


## Contribuição

Se você quiser contribuir para este projeto, por favor, siga estas etapas:

Faça um fork do repositório no GitHub.
Crie uma nova branch com um nome descritivo para a sua funcionalidade ou correção.
Faça as suas alterações no código, seguindo as boas práticas de desenvolvimento e o estilo de código existente.
Escreva testes para verificar o funcionamento da sua funcionalidade ou correção.
Faça um commit e um push das suas alterações para o seu repositório.
Abra um pull request para o repositório original, descrevendo as suas mudanças e o motivo delas.


## Licenças e créditos

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

Este projeto foi desenvolvido durante o curso Explorer da Rocketseat, uma plataforma de educação em tecnologia que ensina as melhores práticas e ferramentas do mercado.

## Contato

Se você tiver alguma dúvida, sugestão ou feedback sobre o projeto, entre em contato com o desenvolvedor:

- [Tiago Lucas da Silva](https://github.com/HomerMau)
- [LinkedIn](https://www.linkedin.com/in/tiagolucasdasilva/)