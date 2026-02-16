# 🧪 Casos de Teste: Módulo de Autenticação

Este documento detalha os cenários de teste para a funcionalidade de login do sistema OrangeHRM.

---

## 1. Testes Funcionais (Autenticação)
> Focados em validar se a lógica de negócio está funcionando conforme os requisitos.

### CT-AUT-01: Validar autenticação com sucesso (Caminho Feliz)
**Descrição:** Verificar se o colaborador consegue acessar o sistema utilizando credenciais válidas.  
**Pré-condições:** Possuir um usuário previamente cadastrado; Ambiente de testes acessível.  
**Pós-condições:** Usuário autenticado e visualizando a Dashboard principal.

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Acessar a URL do OrangeHRM | A página deve carregar sem erros, exibindo os campos de Username e Password. |
| 2 | Clicar no campo "Username" | O campo deve ficar disponivel para digitação. |
| 3 | Inserir um login válido no campo "Username" | O campo deve aceitar o texto e exibi-lo corretamente. |
| 4 | Clicar no campo "Password" | O campo deve ficar disponivel para digitação. |
| 5 | Inserir uma senha válida no campo "Password" | O campo deve aceitar os dados e exibir os caracteres mascarados por segurança. |
| 6 | Clicar no botão "Login" | O sistema deve autenticar o usuário e redirecioná-lo para a Home Page (/dashboard). |

---

### CT-AUT-02: Validar login com credenciais inválidas
**Descrição:** Verificar se o sistema impede o acesso ao informar usuário ou senha incorretos.  
**Pré-condições:** Ambiente de testes acessível.  
**Pós-condições:** O sistema deve permanecer na tela de login e exibir mensagem de erro.

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Acessar a URL do OrangeHRM | Página carregada com sucesso. |
| 2 | Inserir um usuário inexistente ou senha incorreta | O sistema deve permitir a inserção dos dados. |
| 3 | Clicar no botão "Login" | O sistema deve exibir a mensagem de erro: "Invalid credentials" e não permitir o acesso. |

---

### CT-AUT-03: Validar obrigatoriedade de campos (Campos Vazios)
**Descrição:** Verificar se o sistema identifica campos não preenchidos durante a tentativa de login.  
**Pré-condições:** Ambiente de testes acessível.  
**Pós-condições:** Mensagens de alerta devem ser exibidas abaixo dos respectivos campos.

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Acessar a URL do OrangeHRM | Página carregada com sucesso. |
| 2 | Deixar os campos "Username" e "Password" vazios | Campos devem estar limpos. |
| 3 | Clicar no botão "Login" | O sistema não deve processar o login e deve exibir a mensagem "Required" abaixo de ambos os campos. |

## 2. Testes de Usabilidade e Acessibilidade (Não-Funcionais)
> Focados na experiência do colaborador e facilidade de navegação.

---

### CT-USA-01: Validar navegação sequencial via tecla "TAB".
**Descrição:** Garantir que o foco do teclado siga uma ordem lógica (Username > Password > Login).  
**Pré-condições:** Página de login do OrangeHRM carregada.  
**Pós-condições:** O foco deve percorrer todos os elementos interativos na ordem correta.

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Clicar na tecla "TAB" uma vez | O cursor de inserção de piscar indicando que esta dentro do campo "Username". |
| 2 | Clicar novamente na tecla "TAB" | O cursor de inserção deve postar indicando que esta dentro do campo "Password". |
| 3 | Clicar novamente na tecla "TAB" | O foco de teclado deve ser direcionado para o botão "Login". |

---

### CT-USA-02: Validar submissão do formulário via tecla "ENTER"
**Descrição:** Verificar se o sistema permite realizar o login sem a necessidade de clicar com o mouse.  
**Pré-condições:** Campos de Username e Password preenchidos com dados válidos.  
**Pós-condições:** Usuário autenticado com sucesso.

| Passo | Ação | Resultado Esperado |
| :--- | :--- | :--- |
| 1 | Com o foco no campo "Password", pressionar a tecla "TAB" | O foco de teclado deve ser direcionado para o botão "Login" |
| 2 | Com o foco no botão "Login", pressionar a tecla "ENTER" | sistema deve submeter os dados e realizar a autenticação. |