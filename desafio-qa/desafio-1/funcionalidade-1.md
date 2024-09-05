# Desafio 1

## Funcionalidade 1: Cadastro de Novos Restaurantes

### Plano de Testes

**Objetivo**: Validar o processo de cadastro de novos restaurantes no sistema para garantir que todos os requisitos e regras de negócio sejam atendidos.

**Escopo**:
- Verificar a validação dos campos obrigatórios e a integridade das informações fornecidas.
- Garantir que o sistema valide o CNPJ e não permita duplicidades.

### Casos de Teste

| Nº Caso de Teste | Pré-condições | Passos | Resultado Esperado |
|------------------|---------------|--------|--------------------|
| CT01 (Falha)     | NA            | 1. Acessar o painel de administração.<br>2. Selecionar "Cadastro de restaurantes".<br>3. Não preencher os campos obrigatórios.<br>4. Clicar em "Salvar". | Mensagem de erro informando que todos os campos obrigatórios devem ser preenchidos. |
| CT02 (Sucesso)   | NA            | 1. Acessar o painel de administração.<br>2. Selecionar "Cadastro de restaurantes".<br>3. Preencher todos os campos obrigatórios com dados válidos.<br>4. Clicar em "Salvar". | Mensagem de confirmação e redirecionamento para a lista de restaurantes cadastrados. |
| CT03 (Falha)     | NA            | 1. Acessar o painel de administração.<br>2. Selecionar "Cadastro de restaurantes".<br>3. Preencher todos os campos obrigatórios com um CNPJ fictício (ex.: 123.456.789-10).<br>4. Clicar em "Salvar". | Mensagem de erro informando que o CNPJ é inválido. |
| CT04 (Falha)     | NA            | 1. Acessar o painel de administração.<br>2. Selecionar "Cadastro de restaurantes".<br>3. Preencher todos os campos obrigatórios com um CNPJ que contém letras e símbolos.<br>4. Clicar em "Salvar". | Mensagem de erro informando que o CNPJ é inválido. |
| CT05 (Falha)     | NA            | 1. Acessar o painel de administração.<br>2. Selecionar "Cadastro de restaurantes".<br>3. Preencher todos os campos obrigatórios com um CNPJ com comprimento inválido (menos ou mais de 14 caracteres).<br>4. Clicar em "Salvar". | Mensagem de erro informando que o CNPJ é inválido. |
| CT06 (Falha)     | Um restaurante já cadastrado com um CNPJ específico | 1. Acessar o painel de administração.<br>2. Selecionar "Cadastro de restaurantes".<br>3. Preencher todos os campos obrigatórios com o mesmo CNPJ de um restaurante já cadastrado.<br>4. Clicar em "Salvar". | Mensagem de erro informando que o CNPJ já está cadastrado. |
| CT07 (Sucesso)   | NA            | 1. Acessar o painel de administração.<br>2. Selecionar "Cadastro de restaurantes".<br>3. Preencher todos os campos obrigatórios com um CNPJ válido e único.<br>4. Clicar em "Salvar". | Mensagem de confirmação e redirecionamento para a lista de restaurantes cadastrados. |