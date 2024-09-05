# Desafio 2

## Funcionalidade: Cadastro de Entregadores

### Descrição do Bug

Durante o processo de cadastro de entregadores no sistema, foi identificado um bug crítico: o sistema permite que um CPF inválido seja inserido e finaliza o cadastro normalmente, sem exibir nenhuma mensagem de erro. Este problema afeta a integridade dos dados e pode comprometer a segurança e a confiabilidade do sistema.

### Regras de Negócio

- O nome do entregador deve ter no mínimo 3 caracteres e no máximo 50.
- O e-mail deve ser válido e estar no formato correto (exemplo: teste@teste.com).
- O CPF deve ser válido e não pode já ter sido cadastrado no sistema.
- O telefone deve ter o formato (99) 99999-9999.
- A placa do veículo deve ter o formato AAA-9999 ou AAA9A99.
- O modelo do veículo deve ter no máximo 20 caracteres.
- A foto do veículo é opcional.

### Bug Encontrado

- **Descrição**: O sistema permite o cadastro de entregadores com CPF inválido (ex.: 123.456.789-10 ou gerado de forma aleatória) e não exibe mensagem de erro.
- **Impacto**: Alto. Permite que entregadores com CPF inválido sejam cadastrados, afetando a segurança e a integração com outras ferramentas, como o sistema de emissão de notas fiscais.

### Criação do Card no JIRA

**Descrição do Bug**:
O sistema não valida corretamente o CPF durante o cadastro de entregadores, permitindo a inserção de CPFs inválidos e finalizando o cadastro sem apresentar mensagem de erro.

**Pré-condições**:
- Usuário deve estar autenticado no sistema.
- A funcionalidade de cadastro de entregadores deve estar acessível.

**Passos para Reproduzir o Bug**:
1. Acessar a página de cadastro de entregadores.
2. Preencher todos os campos obrigatórios com dados válidos, exceto o CPF, que deve ser inválido (ex.: 123.456.789-10).
3. Clicar no botão de enviar para finalizar o cadastro.

**Resultado Esperado**:
O sistema deve validar o CPF e exibir uma mensagem de erro se o CPF for inválido, impedindo a finalização do cadastro.

**Resultado Obtido**:
O sistema permite o cadastro com CPF inválido e não exibe mensagem de erro.

**Prioridade do Bug**: Alta

**Possíveis Impactos no Sistema**:
- Permite a inserção de dados inválidos, comprometendo a integridade e a segurança do sistema.
- Pode afetar a integração com sistemas externos, como a emissão de notas fiscais.
- Pode levar a problemas legais e operacionais devido a informações inválidas.

### Ações Após a Criação do Card no JIRA

1. **Notificar a Equipe de Desenvolvimento**:
   - Notificar Bruno, o desenvolvedor back-end responsável pela funcionalidade de cadastro de entregadores.
   - Descrever o bug e fornecer evidências (fotos e vídeos) anexadas ao card.

2. **Notificar a Desenvolvedora Front-End**:
   - Informar Ana sobre a necessidade de validações no front-end para a verificação do CPF e para o bloqueio de inputs inválidos.
   - Garantir que as validações necessárias sejam implementadas e testadas.

3. **Comunicar a Gerência de Projeto**:
   - Informar Carol, a gerente de projeto, sobre o bug encontrado e seu impacto no sistema.
   - Discutir a prioridade e as possíveis consequências do bug para o andamento do projeto.

4. **Acompanhar o Processo**:
   - Acompanhar o status do card no JIRA e garantir que o bug seja corrigido e testado adequadamente.
   - Verificar se as correções foram implementadas corretamente e realizar testes para validar a solução.

5. **Atualizar Documentação**:
   - Atualizar a documentação do sistema para refletir as correções realizadas e as mudanças implementadas.