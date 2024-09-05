# Desafio 1

## Funcionalidade 2: Cadastro de Cardápios

### Plano de Testes

**Objetivo**: Validar o processo de cadastro de novos cardápios no sistema para garantir que todos os requisitos e regras de negócio sejam atendidos.

**Escopo**:
- Verificar a validação dos campos obrigatórios e a integridade das informações fornecidas.
- Garantir que o sistema não permita duplicidades de cardápios para o mesmo restaurante e que os preços sejam válidos.

### Casos de Teste

| Nº Caso de Teste | Pré-condições | Passos | Resultado Esperado |
|------------------|---------------|--------|--------------------|
| CT01 (Falha)     | Restaurante cadastrado | 1. Acessar a página de cadastro de cardápios.<br>2. Selecionar o restaurante desejado.<br>3. Não preencher o nome do cardápio.<br>4. Preencher a descrição.<br>5. Preencher os campos obrigatórios para os itens do cardápio.<br>6. Clicar em "Salvar". | Mensagem de erro informando que o nome do cardápio é obrigatório. |
| CT02 (Falha)     | Restaurante cadastrado | 1. Acessar a página de cadastro de cardápios.<br>2. Selecionar o restaurante desejado.<br>3. Preencher o nome do cardápio.<br>4. Não preencher a descrição.<br>5. Preencher os campos obrigatórios para os itens do cardápio.<br>6. Clicar em "Salvar". | Mensagem de erro informando que a descrição do cardápio é obrigatória. |
| CT03 (Falha)     | Restaurante cadastrado | 1. Acessar a página de cadastro de cardápios.<br>2. Selecionar o restaurante desejado.<br>3. Preencher o nome do cardápio.<br>4. Preencher a descrição.<br>5. Preencher o nome de um item do cardápio.<br>6. Não preencher o preço do item.<br>7. Clicar em "Salvar". | Mensagem de erro informando que o preço do item é obrigatório. |
| CT04 (Falha)     | Restaurante cadastrado | 1. Acessar a página de cadastro de cardápios.<br>2. Selecionar o restaurante desejado.<br>3. Preencher o nome do cardápio.<br>4. Preencher a descrição.<br>5. Preencher um item com preço inválido (ex.: texto ou valor negativo).<br>6. Clicar em "Salvar". | Mensagem de erro informando que o preço do item é inválido. |
| CT05 (Falha)     | Restaurante cadastrado com cardápio já existente | 1. Acessar a página de cadastro de cardápios.<br>2. Selecionar o restaurante desejado.<br>3. Preencher um novo cardápio com o mesmo nome de um cardápio já cadastrado para o mesmo restaurante.<br>4. Clicar em "Salvar". | Mensagem de erro informando que já existe um cardápio com o mesmo nome para o restaurante. |
| CT06 (Sucesso)   | Restaurante cadastrado | 1. Acessar a página de cadastro de cardápios.<br>2. Selecionar o restaurante desejado.<br>3. Preencher o nome do cardápio.<br>4. Preencher a descrição.<br>5. Preencher todos os itens do cardápio com dados válidos.<br>6. Clicar em "Salvar". | Mensagem de confirmação e redirecionamento para a lista de cardápios cadastrados. |