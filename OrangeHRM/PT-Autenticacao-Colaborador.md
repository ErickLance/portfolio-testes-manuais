# 📑 Plano de Testes: Autenticação de Colaborador

**Versão:** 1.0  
**Responsável:** Erick Lance

---

## 1. Descrição do Plano
Este documento descreve a estratégia de teste para o módulo de autenticação do sistema OrangeHRM. O foco está em garantir que apenas usuários autorizados acessem a plataforma e que o fluxo de recuperação de acesso funcione conforme esperado.

## 2. Objetivo
Validar a integridade do processo de Login, garantindo que as regras de negócio de segurança sejam respeitadas, prevenindo acessos indevidos e assegurando uma experiência de usuário fluida em casos de erro ou esquecimento de senha.

## 3. Ambiente de Execução
* **Tipo de Ambiente:** Ambiente de Testes (Staging/QA).
* **URL:** https://opensource-demo.orangehrmlive.com/
* **Navegadores Homologados:** Google Chrome (Versão mais recente).
* **Resolução de Tela:** 1920x1080 (Desktop).

---

## 4. Escopo dos Testes

### ✅ O que será testado (In Scope)
* Login com credenciais válidas (Admin e ESS).
* Validação de campos obrigatórios (vazios).
* Comportamento com credenciais inválidas (usuário ou senha incorretos).
* Funcionalidade "Forgot your password?".
* Mascaramento de senha.

### ❌ O que não será testado (Out of Scope)
* Performance (tempo de resposta do servidor).
* Segurança contra ataques de força bruta (Brute Force) via script.
* Compatibilidade com navegadores legados (Internet Explorer).

---

## 5. Tipos de Teste Aplicados
* **Testes Funcionais:** Verificar se as funcionalidades operam conforme o requisito.
* **Testes de UI (Interface):** Verificar alinhamento, cores e mensagens de erro.
* **Testes de Usabilidade:** Verificar se o fluxo é intuitivo para o colaborador.