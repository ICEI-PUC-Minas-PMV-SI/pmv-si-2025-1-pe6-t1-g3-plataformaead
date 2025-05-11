# Front-end Web

Na etapa do Front-end Web, fechamos o escopo da aplicação para um portal administrativo, integrando as APIs que demandam privilégios administrativos e gerenciam o conteúdo da plataforma: criação, edição e exclusão de cursos e aulas.

## Projeto da Interface Web

[Descreva o projeto da interface Web da aplicação, incluindo o design visual, layout das páginas, interações do usuário e outros aspectos relevantes.]

### Wireframes

[Inclua os wireframes das páginas principais da interface, mostrando a disposição dos elementos na página.]

### Design Visual

[Descreva o estilo visual da interface, incluindo paleta de cores, tipografia, ícones e outros elementos gráficos.]

## Fluxo de Dados

[Diagrama ou descrição do fluxo de dados na aplicação.]

## Tecnologias Utilizadas
- Vue.js

## Considerações de Segurança

As regras de segurança para o front-end são baseadas na autenticação e autorização implementadas na etapa de desenvolvimento de APIs. Nesta etapa, as APIs foram integradas com o front-end com configurações de CORS - Cross-Origin Resource Sharing.

## Testes
Testes de integração realizados com a identidade visual ainda incompleta.

### CT 1 - Login com usuário administrativo - OK

**DADO QUE** um usuário possui nome de usuário e senha

**E** privilégios administrativos

**QUANDO** ele fizer o login

**ENTÃO** ele será direcionado para a área de gestão de cursos e aulas

![image](./img/testes-front/CT1-01.png)
![image](./img/testes-front/CT1-02.png)
![image](./img/testes-front/CT1-03.png)

---

### CT 2 - Listar cursos - OK

**DADO QUE** um usuário está logado

**E** possui privilégios administrativos

**QUANDO** ele acessar a área administrativa

**ENTÃO** ele conseguirá listar todos os cursos cadastrados

![image](./img/testes-front/CT2-01.png)
!

---

### CT 3 - Excluir curso - OK

**DADO QUE** um usuário está logado

**E** possui privilégios administrativos

**QUANDO** ele clicar no botão exlcuir curso

**E** confirmar

**ENTÃO** o curso será excluído

![image](./img/testes-front/CT3-01.png)
![image](./img/testes-front/CT3-02.png)
![image](./img/testes-front/CT3-03.png)

---

### CT 4 - Criar curso - OK

**DADO QUE** um usuário está logado

**E** possui privilégios administrativos

**QUANDO** ele preencher os dados de um novo curso

**E** clicar no botão Salvar Curso

**ENTÃO** o curso será criado

![image](./img/testes-front/CT4-01.png)
![image](./img/testes-front/CT4-02.png)

---

### CT 5 - Cadastrar aula - OK

**DADO QUE** um usuário está logado

**E** possui privilégios administrativos

**QUANDO** ele clicar para ver as aulas de um curso

**E** preencher os dados de uma nova aula

**ENTÃO** a aula será criada relacionada ao curso selecionado

![image](./img/testes-front/CT5-01.png)
![image](./img/testes-front/CT5-02.png)
![image](./img/testes-front/CT5-03.png)
![image](./img/testes-front/CT5-04.png)

---

### CT 6 - Excluir aula - OK

**DADO QUE** um usuário está logado

**E** possui privilégios administrativos

**QUANDO** ele listar as aulas de um curso

**E** clicar no botão excluir

**E** confirmar

**ENTÃO** a aula será excluída deste curso

![image](./img/testes-front/CT6-01.png)
![image](./img/testes-front/CT6-02.png)
![image](./img/testes-front/CT6-03.png)

---

### CT 7 - Editar curso - OK

**DADO QUE** um usuário está logado

**E** possui privilégios administrativos

**QUANDO** ele listar os cursos

**E** clicar no botão editar

**E** preencher novos dados

**E** clicar no botão salvar

**ENTÃO** o curso será atualizado

![image](./img/testes-front/CT7-01.png)
![image](./img/testes-front/CT7-02.png)
![image](./img/testes-front/CT7-03.png)

---

### CT 8 - Exibir página Sobre - OK

**DADO QUE** um usuário está acessando o site

**QUANDO** ele clicar no menu Sobre no Header

**ENTÃO** será exibida uma página com dados estáticos

![image](./img/testes-front/CT8-01.png)
![image](./img/testes-front/CT8-02.png)


---

