# 🛡️ ServeRest API Test Suite (Postman)

Este repositório contém uma suíte de testes automatizados para a API [ServeRest](https://serverest.dev/), desenvolvida como parte do meu ecossistema. O objetivo é demonstrar o domínio em testes de contrato, validação de regras de negócio e encadeamento de requisições via Postman.

## 🚀 Tecnologias Utilizadas
* **Postman:** Ferramenta de testes de API.
* **JavaScript:** Scripts de validação na aba "Tests".
* **JSON:** Formato de troca de dados.

## 🧠 O que foi testado?
A coleção abrange o ciclo de vida completo (CRUD) de usuários e o fluxo de autenticação:

- **POST (Criar Usuário):** Validação de status 201, mensagem de sucesso e captura dinâmica do `_id`.
- **GET (Buscar Usuário):** Validação de status 200 e integridade dos dados retornados via variável de coleção.
- **PUT (Atualiza Dados do Usuário):** Validação de status 200 e integridade dos dados atualizados na aplicação.
- **DELETE (Excluir Usuário):** Validação de limpeza de base e status code 200.
- **POST (Login):** Autenticação de usuário e extração automatizada do **Token JWT (Bearer)** para uso em rotas protegidas.

## 🛠️ Diferenciais Técnicos Aplicados
* **Dynamic Data:** Uso de variáveis nativas como `{{$randomEmail}}` para garantir que os testes rodem múltiplas vezes sem conflitos de massa.
* **Request Chaining:** Uso de `pm.collectionVariables` para passar dados entre requisições de forma autônoma.
* **Scripts de Validação:** Asserts robustos verificando não apenas o Status Code, mas a estrutura e o conteúdo do JSON de resposta.

## 📥 Como executar
1. Faça o download do arquivo `Nation_ServeRest_API.postman_collection.json` neste repositório.
2. Abra seu Postman e clique em **Import**.
3. Arraste o arquivo baixado.
4. Execute as requisições em sequência ou utilize o **Collection Runner**.

---
*Projeto focado em demonstrar Testes e Automações na API.*
