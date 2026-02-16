# 🔍 Análise de Requisitos - OrangeHRM

Esta etapa consiste no levantamento das funcionalidades e regras de negócio da aplicação para fundamentar a criação dos cenários de teste.

## 1. Visão Geral do Sistema
O OrangeHRM é um sistema de Gestão de Capital Humano (HRM). A versão open-source demo permite gerenciar informações de funcionários, usuários do sistema e configurações de RH.

## 2. Módulos Analisados
Para este projeto, o foco inicial será nos seguintes módulos:

### 2.1 Módulo: Autenticação do colaborador
* **Funcionalidades:** Autenticar colaborador através de credenciais válidas.
* **Regras de Negócio Indentificadas:
    * As credenciais (usuário e senha) devem existir previamente na base de dados.
    * O campo de senha deve mascarar os caracteres por segurança.
    * O sistema deve exibir uma mensagem de erro genérica para login inválido (ex: "Invalid credentials") para evitar engenharia  social.

### 2.2 Módulo: Admin (Gestão de Usuários)
* **Funcionalidade:** Pesquisar usuários existentes.
* **Funcionalidade:** Adicionar novo usuário (Admin ou ESS).
* **Regras de Negócio Identificadas:**
    * O nome do funcionário deve existir previamente no sistema.
    * A senha deve conter no mínimo 8 caracteres.
    * O nome de usuário deve ser único.

### 2.3 Módulo: PIM (Employee List)
* **Funcionalidade:** Adicionar novo funcionário.
* **Funcionalidade:** Upload de foto de perfil.
* **Regras de Negócio Identificadas:**
    * O 'First Name' e 'Last Name' são campos obrigatórios.
    * O 'Employee ID' é gerado automaticamente, mas permite edição.

---

## 3. Matriz de Rastreabilidade (Simulada)
| ID Requisito | Funcionalidade | Prioridade |
| :--- | :--- | :--- |
| REQ-01 | Login no sistema | Crítica |
| REQ-02 | Cadastro de novo usuário Admin | Alta |
| REQ-03 | Pesquisa de funcionários por nome | Média |