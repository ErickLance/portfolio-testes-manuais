# 📄 Especificação de Requisitos de Software (SRS) - OrangeHRM

**Projeto:** Automação e Testes Manuais OrangeHRM  
**Versão:** 1.0  
**Última Atualização:** Fevereiro/2026  
**Status:** Em Desenvolvimento

---

## 1. Introdução
O objetivo deste documento é listar de forma estruturada as funcionalidades e regras de negócio do sistema **OrangeHRM Open Source**, servindo como base (Single Source of Truth) para a elaboração do Plano de Testes e Casos de Teste.

---

## 2. Requisitos Funcionais (RF)

### 🔐 2.1 Módulo: Autenticação (Login)
> Responsável pelo controle de acesso ao sistema.

| ID | Requisito | Descrição / Regra de Negócio | Prioridade |
| :--- | :--- | :--- | :--- |
| **RF-001** | Autenticação Válida | O sistema deve permitir o acesso apenas com usuário e senha cadastrados na base. | Crítica |
| **RF-002** | Bloqueio de Acesso | O sistema deve exibir mensagem de erro "Invalid credentials" para dados incorretos. | Alta |
| **RF-003** | Recuperação de Senha | Deve existir um fluxo de "Forgot your password" que envie link de redefinição. | Média |
| **RF-004** | Logout | O usuário deve conseguir encerrar a sessão a qualquer momento. | Alta |

### 👥 2.2 Módulo: PIM (Gestão de Informações Pessoais)
> Responsável pelo cadastro e manutenção dos dados dos colaboradores.

| ID | Requisito | Descrição / Regra de Negócio | Prioridade |
| :--- | :--- | :--- | :--- |
| **RF-005** | Cadastrar Funcionário | O sistema deve permitir criar um novo funcionário inserindo Nome e Sobrenome. | Crítica |
| **RF-006** | Geração de ID | O "Employee ID" deve ser gerado automaticamente, mas permitir edição manual se necessário. | Média |
| **RF-007** | Campos Obrigatórios | Não deve ser possível salvar um registro sem "First Name" e "Last Name". | Alta |
| **RF-008** | Upload de Foto | O sistema deve permitir upload de imagens (.jpg, .png) no perfil do funcionário. | Baixa |

### ⚙️ 2.3 Módulo: Admin (Gestão de Usuários e Sistema)
> Responsável por criar logins de acesso e definir permissões.
> **Pré-requisito:** O usuário a ser criado deve estar previamente cadastrado no módulo PIM.

| ID | Requisito | Descrição / Regra de Negócio | Prioridade |
| :--- | :--- | :--- | :--- |
| **RF-009** | Criar Usuário Admin | O sistema deve permitir vincular um login a um funcionário existente. | Crítica |
| **RF-010** | Unicidade de Login | O "Username" deve ser único em todo o sistema. | Alta |
| **RF-011** | Validação de Senha | A senha deve ter no mínimo 8 caracteres (regra simulada para teste). | Alta |
| **RF-012** | Pesquisa de Usuário | Deve ser possível filtrar usuários por Username, Role ou Nome do Funcionário. | Média |

---

## 3. Requisitos Não-Funcionais (RNF)
> Características de qualidade do sistema.

| ID | Categoria | Descrição |
| :--- | :--- | :--- |
| **RNF-001** | Usabilidade | O sistema deve permitir navegação via teclado (Tab/Enter) nos formulários principais. |
| **RNF-002** | Compatibilidade | O sistema deve funcionar corretamente no Chrome, Firefox e Edge. |
| **RNF-003** | Performance | O tempo de login não deve exceder 5 segundos em conexões estáveis. |