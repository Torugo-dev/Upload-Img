# Galeria de Fotos com Upload de Imagens

Este projeto é uma aplicação web para upload, exibição e gerenciamento de imagens. Ele utiliza **Node.js**, **Express**, **MongoDB** e **Multer** no backend, e **HTML**, **CSS** e **JavaScript** no frontend.

## Funcionalidades

- Upload de imagens (limite de 5MB).
- Exibição de uma galeria de fotos.
- Exclusão de imagens.
- Visualização de imagens específicas.

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio

2. Instale as dependências:
   ```bash
   npm install

3. Configure o arquivo .env com as variáveis:
   ```bash
   DB_USER=<seu_usuario_mongodb>
   DB_PASS=<sua_senha_mongodb>
   PORT=<porta_desejada>

4. Inicie o servidor:
   ```bash
   npm start

5. Acesse no navegador:
   ```bash
   http://localhost:<porta_configurada_no_env>

## Endpoints da API

- **POST `/pictures`**: Faz upload de uma nova imagem.
- **GET `/pictures`**: Retorna todas as imagens.
- **GET `/pictures/:id/image`**: Retorna a imagem específica pelo ID.
- **DELETE `/pictures/:id`**: Exclui uma imagem pelo ID.

## Funcionalidades do Frontend

- **Carregamento de Imagens**: As imagens são buscadas da API e exibidas em uma galeria.
- **Upload de Imagens**: Um modal permite que o usuário envie novas imagens.
- **Exclusão de Imagens**: Botões de exclusão permitem remover imagens específicas.
- **Notificações**: Mensagens de sucesso ou erro são exibidas para ações realizadas.

## Estrutura do Banco de Dados

O banco de dados MongoDB utiliza o seguinte esquema para armazenar imagens:

```javascript
{
  name: String, // Nome da imagem
  image: Buffer, // Dados da imagem
  contentType: String // Tipo de conteúdo (ex.: image/png)
}
```



