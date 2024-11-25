# Projeto Integrador:
# Desenvolvimento de Sistemas Orientado a Objetos

Esse é o repositório oficial do Projeto Integrador 2ª entrega do Grupo 19.

Nossa solução consiste em um sistema para administração de dados de uma universidade.

A solução apresentada consiste na modelagem de um sistema voltado para a gestão de dados de uma universidade. Foi desenvolvida utilizando diagramas da UML (Linguagem de Modelagem Unificada).
Em especial, representa o cadastro de diferentes tipos de pessoas que vão interagir com o sistema.
Cadastros de:

*   Pessoa Física
*   Pessoa Jurídica
*   Professores
*   Fornecedores
*   Alunos

A apresentação dos diagramas UML ajuda as pessoas de negócio e desenvolvedores a terem uma visão do software a ser desenvolvido.
A utilização da POO (Programação Orientada a Objetos) traz grandes vantagens, entre as quais podemos destacar:
1.  Reutilização e manutenção do código
2.  Organização e modularização do sistema
3.  Programas mais escaláveis e flexíveis
4.  Modelagem realista


Visão Geral da Solução Proposta:
A proposta de implementação do sistema visa uma série de benefícios significativos para a faculdade. Primeiramente, a centralização das informações permite o acesso rápido e eficiente aos dados, facilitando a administração e melhorando a experiência dos usuários. Além disso, a interação entre alunos, professores e os demais envolvidos será realizada de maneira simplificada, promovendo um ambiente acadêmico mais colaborativo e engajado.
A possibilidade de gerar relatórios, análises detalhadas sobre o desempenho acadêmico dos alunos e a gestão de fornecedores também são aspectos muito importantes para a instituição, principalmente para a tomada de decisões estratégicas e melhoria de processos.

---

|**Caso de Uso: UC001 - Manter Cadastro de Pessoa Física**|
|---|
Ator Principal: Administrador Escolar
Descrição: Como o administrador escolar pode criar, atualizar, visualizar e excluir o
cadastro de uma pessoa física no sistema de gestão escolar.
||
*Pré-condição:*
Administrador escolar deve estar autenticado no sistema com permissões adequadas para manter cadastros de pessoas físicas.
||
*Fluxo Principal:*
|1. Administrador clica em "Cadastros" e seleciona a opção "Pessoa Física".
|2. Sistema apresenta uma lista de cadastros de pessoas físicas já existentes.
|3. Administrador clica em "Novo Cadastro" para criar um novo cadastro ou seleciona um cadastro existente para atualização.
|4. Sistema apresenta um formulário de cadastro solicitando as seguintes informações (nome completo, CPF, data de nascimento, endereço de e-mail, telefone e endereço).
|5. Administrador preenche ou atualiza as informações no formulário.
|6. Administrador clica em "Salvar" para armazenar informações no banco de dados.
|7. Sistema valida informações inseridas (número do CPF, e-mail único, etc).
|8. Sistema salva ou atualiza o cadastro no banco de dados.
|9. Sistema confirma a ação e notifica o administrador do sucesso da operação.
||
*Fluxo Alternativo:*
|1. Passo 3a: Se o administrador desejar excluir um cadastro, ele seleciona o cadastro na lista, clica em "Excluir" e o sistema solicita uma confirmação antes de remover os dados do banco de dados.
|2. Passo 7a: Se o CPF ou e-mail já estiverem cadastrados, o sistema informa o usuário que já existe uma conta com este CPF ou e-mail cadastrados.
||
*Pós-condições:*
|1. O cadastro de pessoa física foi criado, atualizado ou excluído conforme ação realizada pelo administrador.
|2. Informações da pessoa física são armazenadas de forma segura no BD.
|3. O sistema reflete as alterações imediatamente.

---

|**Caso de Uso: UC002 - Manter Cadastro de Pessoa Jurídica**|
|---|
|Ator Principal: Administrador Escolar
|Descrição: Como o administrador escolar pode criar, atualizar, visualizar e excluir o
|cadastro de uma pessoa jurídica no sistema de gestão escolar.
|Pré-condição: O administrador escolar deve estar autenticado no sistema com permissões adequadas para manter cadastros de pessoas jurídicas.
||
*Fluxo Principal:*
|1. Administrador clica em "Cadastros" e seleciona a opção "Pessoa Jurídica".
|2. Sistema apresenta uma lista de cadastros de pessoas jurídicas já existentes.
|3. Administrador clica em "Novo Cadastro" para criar um novo cadastro ou seleciona um cadastro existente para atualização.
|4. Sistema apresenta formulário de cadastro com os campos: razão social, CNPJ, nome fantasia, e-mail, telefone, endereço e responsável pela empresa.
|5. Administrador preenche ou atualiza as informações no formulário.
|6. Administrador clica em "Salvar" para armazenar as informações no BD.
|7. Sistema valida as informações inseridas (CNPJ, e-mail único, etc.).
|8. Sistema salva ou atualiza o cadastro no banco de dados.
|9. Sistema confirma a ação e notifica o administrador do sucesso da operação.
||
*Fluxo Alternativo:*
|1. Passo 3a: Se o administrador desejar excluir um cadastro, ele seleciona o cadastro na lista, clica em "Excluir" e o sistema solicita confirmação antes de remover os dados do banco de dados.
|2. Passo 7a: Se o CNPJ ou e-mail já estiverem cadastrados, sistema informa o usuário e sugere que recupere sua senha ou utilize outro e-mail para cadastro.
||
*Pós-condições:*
|1. O cadastro de pessoa física foi criado, atualizado ou excluído conforme ação realizada pelo administrador.
|2. As informações da pessoa física estão armazenadas de forma segura no BD.
|3. O sistema reflete as alterações imediatamente.


---

|**Caso de Uso: UC003 - Manter Cadastro de Professor**|
|---|
Ator Principal: Administrador Escolar
Descrição: Descreve como o administrador escolar pode criar, atualizar, visualizar e excluir o cadastro de um professor no sistema de gestão escolar, utilizando um cadastro de pessoa física já existente no sistema.
||
*Pré-condição:*
|1. O administrador escolar deve estar autenticado no sistema com permissões adequadas para gerenciar cadastros de professores.
|2. O cadastro de pessoa física do professor deve existir no sistema antes de realizar a operação.
||
*Fluxo Principal:*
|1. Administrador clica em "Cadastros" e seleciona a opção "Professor".
|2. Sistema apresenta uma lista de cadastros de professores já existentes.
|3. Administrador clica em "Novo Cadastro" para criar um novo cadastro ou seleciona um cadastro existente para atualização.
|4. Sistema apresenta um formulário de cadastro com os seguintes campos (ID, nome completo, e-mail, endereço, formação e disciplinas).
|5. Administrador preenche ou atualiza as informações no formulário.
|6. Administrador clica em “Salvar” para armazenar informações no BD.
|7. Sistema verifica se a pessoa física selecionada já está associada a um cadastro de professor para evitar duplicidade.
|8. Sistema salva ou atualiza o cadastro no banco de dados.
|9. Sistema confirma a ação e notifica o administrador do sucesso da operação.
||
*Fluxo Alternativo:*
|1. Passo 3a: Se o administrador desejar excluir um cadastro, ele seleciona o cadastro na lista, clica em "Excluir", e o sistema solicita uma confirmação antes de remover os dados do banco de dados.
|2. Passo 3b:
|- Para um novo cadastro, o sistema solicita que o administrador selecione uma pessoa física já cadastrada no sistema.
|- O administrador seleciona a pessoa física correspondente ao professor.
|3. Passo 7a: Se o cadastro de pessoa física já estiver associado a outro cadastro de professor, o sistema alerta o administrador e impede a duplicação.
||
*Pós-condições:*
|1. O cadastro de professor foi criado, atualizado ou excluído conforme a ação realizada pelo administrador.
|2. O cadastro de pessoa física associado permanece intacto, com o vínculo correto estabelecido.
|3. Dados do professor foram armazenadas de forma segura no banco de dados.
|4. O sistema reflete as alterações imediatamente.

---

|**Caso de Uso: UC004 - Manter Cadastro de Fornecedor**|
|---|
Ator Principal: Administrador Escolar
Descrição: Este caso de uso descreve como o administrador escolar pode criar, atualizar, visualizar e excluir o cadastro de um fornecedor no sistema de gestão escolar, utilizando um cadastro de pessoa jurídica já existente no sistema.
||
*Pré-condição:*
|1. O administrador escolar deve estar autenticado no sistema com permissões adequadas para gerenciar cadastros de fornecedores.
|2. O cadastro de pessoa jurídica do fornecedor deve existir no sistema antes de realizar a operação.
||
*Fluxo Principal:*
|1. Administrador clica em "Cadastros" e seleciona a opção "Fornecedor".
|2. O sistema apresenta uma lista de cadastros de fornecedores já existentes.
|3. Administrador clica em "Novo Cadastro" para criar um novo cadastro ou seleciona um cadastro existente para atualização.
|4. Sistema apresenta formulário de cadastro com os campos: ID do fornecedor, tipo de serviço, produto fornecido, dados bancários, método de entrega.
|5. Administrador preenche ou atualiza as informações no formulário.
|6. Administrador clica em "Salvar" para armazenar as informações no banco de dados.
|7. Sistema verifica se a pessoa jurídica selecionada já está associada a um cadastro de fornecedor para evitar duplicidade.
|8. Sistema salva ou atualiza o cadastro no banco de dados.
|9. Sistema confirma a ação e notifica o administrador do sucesso da operação.
||
*Fluxo Alternativo:*
|1. Passo 3a: Se o administrador desejar excluir um cadastro, ele seleciona o cadastro na lista, clica em "Excluir", e o sistema solicita uma confirmação antes de remover os dados do banco de dados.
|2. Passo 3b:
|- Para um novo cadastro, o sistema solicita que o administrador selecione uma pessoa jurídica já cadastrada no sistema.
|- O administrador seleciona a pessoa jurídica correspondente ao fornecedor.
|3. Passo 7a: Se o cadastro de pessoa jurídica já estiver associado a outro cadastro de fornecedor, o sistema alerta o administrador e impede a duplicação.
||
*Pós-condições:*
|1. O cadastro do fornecedor foi criado, atualizado ou excluído conforme a ação realizada pelo administrador.
|2. O cadastro de pessoa jurídica associado permanece intacto com o vínculo correto estabelecido.
|3. Dados do fornecedor são armazenadas de forma segura no banco de dados.
|4. O sistema reflete as alterações imediatamente.

---

|**Caso de Uso: UC005 - Manter Cadastro de Aluno**|
|---|
Ator Principal: Administrador Escolar
Descrição: Descreve como o administrador escolar pode criar, atualizar, visualizar e excluir o cadastro de um aluno no sistema de gestão escolar, utilizando um cadastro de pessoa física já existente no sistema.
||
*Pré-condição:*
|1. O administrador escolar deve estar autenticado no sistema com permissões adequadas para gerenciar cadastros de alunos.
|2. O cadastro de pessoa física do aluno já deve existir no sistema.
||
*Fluxo Principal:*
|1. O administrador clica em "Cadastros" e seleciona a opção "Aluno".
|2. O sistema apresenta uma lista de cadastros de alunos já existentes.
|3. O administrador clica em "Novo Cadastro" para criar um novo cadastro ou seleciona um cadastro existente para atualização.
|4. Sistema apresenta formulário de cadastro com os campos: código do aluno, disciplinas matriculadas, histórico escolar, certificado de conclusão do ensino médio.
|5. O administrador preenche ou atualiza as informações no formulário.
|6. O administrador clica em "Salvar" para armazenar as informações no BD.
|7. O sistema verifica se a pessoa física selecionada já está associada a um cadastro de aluno para evitar duplicidade.
|8. O sistema salva ou atualiza o cadastro no banco de dados.
|9. O sistema confirma a ação e notifica o administrador do sucesso da operação.
||
*Fluxo Alternativo:*
|1. Passo 3a: Se o administrador desejar excluir um cadastro, ele seleciona o cadastro na lista, clica em "Excluir", e o sistema solicita uma confirmação antes de remover os dados do banco de dados.
|2. Passo 3b:
|- Se for um novo cadastro, o sistema solicita que o administrador selecione uma pessoa física já cadastrada no sistema.
|- Se for um cadastro existente, o administrador seleciona a pessoa física correspondente ao fornecedor.
|3. Passo 7a: Se o cadastro de pessoa física já estiver associado a outro cadastro de aluno, o sistema alerta o administrador e impede a duplicação.
||
*Pós-condições:*
|1. O cadastro do aluno foi criado, atualizado ou excluído conforme a ação realizada pelo administrador.
|2. O cadastro de pessoa física associado permanece intacto, com o vínculo correto estabelecido.
|3. Dados do aluno foram armazenados de forma segura no banco de dados.
|4. O sistema reflete as alterações imediatamente.

---

# Diagramas de Classes
![Diagrama de Classes](https://github.com/MauroFBrito/Senac-Grupo19-PI2aEntrega/blob/main/Diagr%20Classes%20Pag1.png)
![Diagrama de Classes](https://github.com/MauroFBrito/Senac-Grupo19-PI2aEntrega/blob/main/Diagr%20Classes%20Pag2.png)

---

*Diagrama de Casos de Uso:*
![Casos de Uso](https://github.com/MauroFBrito/Senac-Grupo19-PI2aEntrega/blob/main/PI%20-%20Diagramas%20de%20Casos%20de%20Uso3.png?raw=true)


---

# *Interface*

A interface foi projetada com o objetivo de proporcionar uma interação intuitiva e eficiente, onde o usuário consiga realizar suas tarefas de forma rápida e sem dificuldades.
As cores escolhidas para o projeto foram preto, branco e cinza como cores principais e laranja como cor de destaque.
A aplicação é responsiva, ou seja, a interface se adapta a desktops, tablets e celulares, por exemplo. 
A seguir iremos demonstrar algumas páginas da interface incluindo imagens para ilustrar as descrições.

# Tela inicial:
A tela inicial apresenta, no cabeçalho, um botão de Menu, um de acesso do Aluno e outro de Cadastros. Abaixo, no corpo da página, são exibidas mensagens selecionadas pelo administrador do sistema e, no rodapé, temos os ícones de redes sociais onde a Universidade tem páginas (Instagram, Youtube e LinkedIn).
A partir da tela inicial, podemos acessar a página de login dos alunos, por exemplo, pelo botão Aluno, conforme imagem a seguir. Na página de login temos o formulário de acesso com os campos de E-mail e Senha, o botão de Entrar e a opção de ‘Esqueceu sua senha?’ logo ao final do formulário.


![Tela inicial mobile](https://github.com/MauroFBrito/Senac-Grupo19-PI2aEntrega/blob/main/Tela%20inicial%20mobile%20ajustada.jpeg)



# Tela de Cadastro Geral:
Esta tela apresenta, no cabeçalho, o nome da Universidade e um menu com a mensagem ‘Olá, [nome do usuário]’, onde o usuário pode clicar/tocar em cima e aparecem mais opções. No corpo da página temos uma tabela com as informações dos usuários já cadastrados, abaixo um campo de pesquisa e após os botões: Relatórios, Excluir, Editar e Novo Cadastro.

![Tela Cadastros Gerais](https://github.com/MauroFBrito/Senac-Grupo19-PI2aEntrega/blob/main/Cadastros%20Gerais.png)



# Novo Cadastro:
Nesta tela o usuário com perfil de administrador poderá incluir um novo cadastro. A tela apresenta o mesmo cabeçalho da tela de Cadastro Geral. No corpo da página temos o título ‘Novo Cadastro’ seguido das opções de cadastro para Pessoa Física (Aluno ou Professor) e de Pessoa Jurídica (Fornecedor). Abaixo temos o formulário de cadastro, campo para pesquisa e os botões Relatórios, Excluir, Editar e Novo Cadastro.

*Novo Cadastro Aluno*
![Tela Novo Cadastro Aluno](https://github.com/MauroFBrito/Senac-Grupo19-PI2aEntrega/blob/main/Novo%20Cadastro%20-%20Pessoa%20F%C3%ADsica%20(Aluno).png)

*Novo Cadastro Professor*
![Tela Novo Cadastro Professor](https://github.com/MauroFBrito/Senac-Grupo19-PI2aEntrega/blob/main/Novo%20Cadastro%20-%20Pessoa%20F%C3%ADsica%20(Professor).png)

*Novo Cadastro Pessoa Jurídica*
![Tela Novo Cadastro Pessoa Jurídica](https://github.com/MauroFBrito/Senac-Grupo19-PI2aEntrega/blob/main/Novo%20Cadastro%20-%20Pessoa%20Jur%C3%ADdica.png)

Os componentes da interface foram projetados para que o usuário possa acessar facilmente as funcionalidades disponíveis. A utilização de cores foi feita de forma que garantisse o contraste necessário para que o usuário localize os botões e navegue pelas funcionalidades necessárias facilmente.

---

# Conclusão

A implementação deste sistema tem como intuito uma série de melhorias operacionais e administrativas para a faculdade, contribuindo para um ambiente mais organizado e produtivo. Ao facilitar o acesso e a gestão das informações de alunos, professores e fornecedores, a instituição poderá focar no seu principal objetivo: oferecer educação de qualidade.

---

# REFERÊNCIAS

OLIVEIRA, Henrique Pontes Gonçalves de. Análise de sistemas. São Paulo: Editora Senac São Paulo, 2019. (Série Universitária). Disponível em: <https://senacsp.blackboard.com/ultra/courses/_251987_1/cl/outline>. Acesso em: 23 set. 2024.

LEAL, Enoque. Projeto Integrador [Apresentação]. São Paulo: SENAC EAD, 2024. Disponível em: <https://senacsp.blackboard.com/ultra/courses/_251987_1/cl/outline>. Acesso em: 23 set. 2024.


---

