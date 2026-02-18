---

## 2. Testes Funcionais (Módulo PIM - Gestão de Funcionários)
> **Objetivo:** Validar o cadastro e gerenciamento de colaboradores. Esses dados são pré-requisitos para a criação de usuários no módulo Admin.

---

## 2. Testes Funcionais (Módulo PIM - Gestão de Funcionários)
> **Objetivo:** Validar o cadastro e gerenciamento de colaboradores. Esses dados são pré-requisitos para a criação de usuários no módulo Admin.

### CT-PIM-01: Cadastrar novo funcionário com sucesso (Sem nova credencial)
**Rastreabilidade:** Cobre os requisitos `RF-005` e `RF-006`.  
**Descrição:** Verificar se é possível criar um funcionário preenchendo apenas os dados obrigatórios.  
**Pré-condições:** Estar logado como Admin.  
**Pós-condições:** Funcionário salvo e exibido na lista de empregados.

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Acessar o menu "PIM" > "Add Employee" | O formulário de cadastro deve ser exibido. |
| 2 | Preencher "First Name" e "Last Name" | O sistema deve aceitar caracteres alfabéticos. |
| 3 | Verificar o campo "Employee Id" | O campo deve vir preenchido automaticamente, mas permitir edição. |
| 4 | Clicar no botão "Save" | O sistema deve exibir a mensagem "Successfully Saved" e redirecionar para o perfil do funcionário (Personal Details). |

---

### CT-PIM-02: Cadastrar novo funcionario com sucesso (Com nova credencial)
**Rastreabilidade:** Cobre os requisitos `RF-005` e `RF-006`.  
**Descrição:** Verificar se é possível criar um funcionário preenchendo apenas os dados obrigatórios e informando dados de login.  
**Pré-condições:** Estar logado como Admin; Campos "First Name" e "Last Name" previamente preenchidos.
**Pós-condições:** Funcionário salvo, exibido na lista de empregados e com credenciais salvas no banco de dados.

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Acessar o menu "PIM" > "Add Employee" | O formulário de cadastro deve ser exibido. |
| 2 | Habilitar a flag "Create Login Details" | O sistema deve exbir o fomulario de login |
| 3 | Preencher o campo "Username", "Password" e "Confirm Password" | O campo deve aceitar os dados preenchidos |
| 4 | Clicar no botão "Save" | O sistema deve exibir a mensagem "Successfully Saved" e redirecionar para o perfil do funcionário (Personal Details). |

---

### CT-PIM-02: Validar obrigatoriedade de campos (First e Last Name)
**Rastreabilidade:** Cobre o requisito `RF-007`.  
**Descrição:** Garantir que o sistema impeça o cadastro de funcionários sem identificação de nome.  
**Pré-condições:** Acessar a tela "Add Employee".

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Deixar os campos "First Name" e "Last Name" em branco | Campos vazios. |
| 2 | Clicar no botão "Save" | O sistema deve exibir a mensagem de erro "Required" em vermelho abaixo dos campos obrigatórios e não salvar o registro. |

---

### CT-PIM-03: Pesquisar funcionário recém-criado
**Rastreabilidade:** Validação de Integridade de Dados.  
**Descrição:** Confirmar se o funcionário criado aparece na listagem geral e se os dados persistem.  
**Pré-requisito:** Ter executado o CT-PIM-01 com sucesso (anotar o ID ou Nome).

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Clicar no menu "Employee List" | A lista de filtros deve ser exibida. |
| 2 | Digitar o nome do funcionário criado no campo "Employee Name" | O sistema deve sugerir o nome via auto-complete. |
| 3 | Clicar em "Search" | A tabela deve exibir o registro do funcionário com o status correto. |

---

### CT-PIM-02: Validar obrigatoriedade de campos (First e Last Name)
**Rastreabilidade:** Cobre o requisito `RF-007`.  
**Descrição:** Garantir que o sistema impeça o cadastro de funcionários sem identificação de nome.  
**Pré-condições:** Acessar a tela "Add Employee".

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Deixar os campos "First Name" e "Last Name" em branco | Campos vazios. |
| 2 | Clicar no botão "Save" | O sistema deve exibir a mensagem de erro "Required" em vermelho abaixo dos campos obrigatórios e não salvar o registro. |

---

### CT-PIM-03: Pesquisar funcionário recém-criado
**Rastreabilidade:** Validação de Integridade de Dados.  
**Descrição:** Confirmar se o funcionário criado aparece na listagem geral e se os dados persistem.  
**Pré-requisito:** Ter executado o CT-PIM-01 com sucesso (anotar o ID ou Nome).

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Clicar no menu "Employee List" | A lista de filtros deve ser exibida. |
| 2 | Digitar o nome do funcionário criado no campo "Employee Name" | O sistema deve sugerir o nome via auto-complete. |
| 3 | Clicar em "Search" | A tabela deve exibir o registro do funcionário com o status correto.