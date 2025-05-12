# Front-end Web

Na etapa do Front-end Web, fechamos o escopo da aplicação para um portal administrativo, integrando as APIs que demandam privilégios administrativos e gerenciam o conteúdo da plataforma: criação, edição e exclusão de cursos e aulas.

## Projeto da Interface Web


### Wireframes

## Pagina inicial
![image](https://github.com/user-attachments/assets/27ee77ee-29a9-4d1d-bdfc-a38ee920e36f)

## Pagina Sobre
![image](https://github.com/user-attachments/assets/253acf7d-2a60-4cb3-a795-5026be34ea3a)

## Pagina gerenciar cursos
![image](https://github.com/user-attachments/assets/b447fa41-6eaf-47e9-a44f-510bf46476d5)

## Pagina Login
![image](https://github.com/user-attachments/assets/b362165d-2ba8-4e96-a7b3-60bdf6db4c4a)


### Design Visual

## Cores usadas

Cor usada no header e outras divs principais das paginas ![image](https://github.com/user-attachments/assets/a0100900-8038-4ae2-b31a-8eb2c96c8734) #98BFE5.

Cor usada nos textos e titulos ![image](https://github.com/user-attachments/assets/91221ea7-f2d0-4495-bbbf-d8357f1c9412) #212529.

Cor usada no footer ![image](https://github.com/user-attachments/assets/d92a45cc-b02f-4d9b-9af6-1f04d22c0e76) #101D42.

Cor usada nos textos do footer ![image](https://github.com/user-attachments/assets/cd42875e-da7a-4b0f-be5a-dd3ed092a2c1) #6F8FB4.

Cor usada nos textos secundarios do footer e botões ![image](https://github.com/user-attachments/assets/e3d377dd-6d8c-42f8-a39f-0cc88da6a7bc) #F4D35E.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Tipografia
Usado Segoe UI em todos os titulos e paragragos do site.
Oswavld usado nos botões.

## Ícones
![user](https://github.com/user-attachments/assets/bfe23755-bbc4-4386-bdc1-ef33e295cb13) Usado no login.

![search](https://github.com/user-attachments/assets/e7a6e92f-29d5-4a7c-bced-508bf704322a) Usado pós barra de pesquisa.

## Logo
Logo do nosso projeto. Eduteck
![logoBranca](https://github.com/user-attachments/assets/76952016-14ba-4eeb-a196-5d96f6a27bad) 


## Fluxo de Dados

[Diagrama ou descrição do fluxo de dados na aplicação.]

## Tecnologias Utilizadas
- HTML
- CSS
- JavaScript
- Vue.js

## Considerações de Segurança

A autenticação dos usuários é realizada por meio do login com e-mail e senha, onde o Keycloak atua como provedor de identidade, emitindo um token de acesso (JWT) após a validação das credenciais. Esse token é então utilizado pelo front-end para acessar recursos protegidos nas APIs, garantindo que apenas usuários autenticados e devidamente autorizados tenham permissão para consumir os dados ou realizar ações específicas.

Além disso, foram aplicadas configurações de CORS (Cross-Origin Resource Sharing) nas APIs, permitindo que o front-end se comunique com os serviços de backend de forma segura, mesmo estando hospedado em domínios distintos.

Essas medidas em conjunto asseguram uma comunicação segura entre o front-end e o backend, protegendo tanto os dados dos usuários quanto a integridade da aplicação como um todo.

## Testes
Testes de integração realizados com a identidade visual ainda incompleta.

### CT 1 - Login com usuário administrativo - OK

**DADO QUE** um usuário possui nome de usuário e senha

**E** privilégios administrativos

**QUANDO** ele fizer o login

**ENTÃO** ele será direcionado para a área de gestão de cursos e aulas

![image](./img/testes-front/teste-login01.png)

![image](./img/testes-front/teste-login02.png)

![image](./img/testes-front/teste-login03.png)

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

