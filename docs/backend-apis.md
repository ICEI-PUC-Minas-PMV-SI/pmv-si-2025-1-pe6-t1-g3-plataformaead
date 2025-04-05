# APIs e Web Services

O planejamento de uma aplicação de APIS Web é uma etapa fundamental para o sucesso do projeto. Ao planejar adequadamente, você pode evitar muitos problemas e garantir que a sua API seja segura, escalável e eficiente.

Aqui estão algumas etapas importantes que devem ser consideradas no planejamento de uma aplicação de APIS Web.

[Inclua uma breve descrição do projeto.]

## Objetivos da API

O primeiro passo é definir os objetivos da sua API. O que você espera alcançar com ela? Você quer que ela seja usada por clientes externos ou apenas por aplicações internas? Quais são os recursos que a API deve fornecer?

[Inclua os objetivos da sua api.]


## Modelagem da Aplicação
[Descreva a modelagem da aplicação, incluindo a estrutura de dados, diagramas de classes ou entidades, e outras representações visuais relevantes.]

![image](./img/modelagemEixo6-EntidadeRelacionamento.drawio.png)
Diagrama de Entidade Relacionamento com domínios dos serviços


## Tecnologias Utilizadas

Existem muitas tecnologias diferentes que podem ser usadas para desenvolver APIs Web. A tecnologia certa para o seu projeto dependerá dos seus objetivos, dos seus clientes e dos recursos que a API deve fornecer.

[Lista das tecnologias principais que serão utilizadas no projeto.]

## API Endpoints

### BadgeService

#### **POST /badges** - Criar badge
> Cria um novo badge.

**Request Body**
```json
{
  "name": "test",
  "imgUrl": "test"
}
```

**Responses**
- `201 Created`: Badge criado com sucesso.

---

#### **GET /badges** - Listar badges
> Retorna todos os badges disponíveis.

**Responses**
- `200 OK`: Lista de badges.

---

#### **GET /badges/{id}** - Buscar badge por ID
> Retorna um badge específico.

**Path Parameters**
- `id`: ID do badge (ex: `2`)

**Responses**
- `200 OK`: Badge encontrado.
- `404 Not Found`: Badge não encontrado.

---

#### **PUT /badges/{id}** - Atualizar badge
> Atualiza um badge existente.

**Request Body**
```json
{
  "name": "Química",
  "imgUrl": "/images/badges/flask.png"
}
```

**Responses**
- `200 OK`: Badge atualizado.
- `404 Not Found`: Badge não encontrado.

---

#### **DELETE /badges/{id}** - Remover badge
> Remove um badge.

**Responses**
- `204 No Content`: Badge removido.
- `404 Not Found`: Badge não encontrado.

---

### StudentPointsService

#### **GET /points** - Ranking de pontos
> Lista todos os estudantes ordenados por pontos.

**Responses**
- `200 OK`: Lista de ranking de pontos.

---

#### **GET /points/{id}** - Pontos de um estudante
> Retorna os pontos de um estudante específico.

**Responses**
- `200 OK`: Dados do estudante.
- `404 Not Found`: Estudante não encontrado.

---

#### **PUT /points/{id}** - Atualizar pontos
> Atualiza os pontos de um estudante.

**Request Body**
```json
{
  "points": "200"
}
```

**Responses**
- `200 OK`: Pontos atualizados.
- `404 Not Found`: Estudante não encontrado.

---

#### **DELETE /points/{id}** - Limpar pontos
> Zera os pontos de um estudante.

**Responses**
- `204 No Content`: Pontos resetados.
- `404 Not Found`: Estudante não encontrado.

---

### StudentBadgeService

#### **POST /studentBadge** - Atribuir badge ao estudante
> Atribui um badge a um estudante.

**Query Params**
- `studentId`: ID do estudante
- `badgeId`: ID do badge

**Responses**
- `201 Created`: Badge atribuído.
- `404 Not Found`: Estudante ou badge não encontrado.

---

#### **GET /studentBadge** - Listar badges de um estudante
> Retorna todos os badges de um estudante.

**Query Params**
- `studentId`: ID do estudante

**Responses**
- `200 OK`: Lista de badges.

---

#### **DELETE /studentBadge** - Remover badge do estudante
> Remove um badge atribuído a um estudante.

**Query Params**
- `studentId`: ID do estudante
- `badgeId`: ID do badge

**Responses**
- `204 No Content`: Remoção concluída.

---

### LessonService

#### **GET /lessons** - Listar aulas
> Retorna todas as aulas.

**Responses**
- `200 OK`: Lista de aulas.

---

#### **POST /lessons** - Criar aula
> Cria uma nova aula.

**Request Body**
```json
{
  "name": "teste 1",
  "description": "teste",
  "videoUrl": "teste"
}
```

**Responses**
- `201 Created`: Aula criada.

---

#### **GET /lessons/{id}** - Buscar aula por ID
> Retorna uma aula específica.

**Responses**
- `200 OK`: Aula encontrada.
- `404 Not Found`: Aula não encontrada.

---

#### **PUT /lessons/{id}** - Atualizar aula
> Atualiza dados de uma aula.

**Request Body**
```json
{
  "name": "teste put",
  "description": "put",
  "videoUrl": "put"
}
```

**Responses**
- `200 OK`: Aula atualizada.
- `404 Not Found`: Aula não encontrada.

---

#### **DELETE /lessons/{id}** - Remover aula
> Remove uma aula específica.

**Responses**
- `204 No Content`: Aula removida.
- `404 Not Found`: Aula não encontrada.

---

## LessonService

### `GET /lessons`
> Lista todas as aulas.

---

### `POST /lessons`
> Cria uma nova aula.

**Request Body:**
```json
{
  "name": "teste 1",
  "description": "teste",
  "videoUrl": "teste"
}
```

---

### `GET /lessons/{id}`
> Retorna dados da aula a partir do ID.

---

### `PUT /lessons/{id}`
> Atualiza a aula a partir do ID.

**Request Body:**
```json
{
  "name": "teste put",
  "description": "put",
  "videoUrl": "put"
}
```

---

### `DELETE /lessons/{id}`
> Remove a aula a partir do ID

---

## CourseService

### `GET /courses`
> Lista todos os cursos.

**Responses**
- `200 OK`: Lista de cursos.

---

### `DELETE /courses?courseId={courseId}&lessonId={lessonId}`
> Remove uma aula de um curso.

**Responses**
- `204 No Content`: Curso atualizado.
- `404 Not Found`: Aula não encontrada.
- `404 Not Found`: Curso não encontrado.

---

### `DELETE /courses/{id}`
> Exclui o curso a partir do ID.

**Responses**
- `204 No Content`: Curso removido.
- `404 Not Found`: Curso não encontrado.

---

### `PUT /courses?courseId={courseId}&lessonId={lessonId}`
> Adiciona uma aula a um curso.

**Responses**
- `204 No Content`: Curso atualizado.
- `404 Not Found`: Aula não encontrada.
- `404 Not Found`: Curso não encontrado.

---

### `GET /courses/{id}`
> Retorna dados do curso a partir do ID.

**Response Body**
```json
{
    "id": 10,
    "name": "teste",
    "description": "teste",
    "coverImgUrl": "teste",
    "lessons": [
            {
        "id": 1,
        "name": "teste 1",
        "description": "teste",
        "videoUrl": "teste"
      }
    ]
}
```
---

### `POST /courses/`
> Cria um novo curso.

**Request Body:**
```json
{
  "name": "teste",
  "description": "teste",
  "coverImgUrl": "teste",
  "lessons": []
}
```
**Responses**
- `200 OK`: Curso criado.


---

### `PUT /courses/{id}`
> Atualiza o curso a partir do ID.

**Request Body:**
```json
{
  "name": "teste",
  "description": "teste",
  "coverImgUrl": "teste",
  "lessons": []
}
```
**Responses**
- `200 OK`: Curso atualizado.
- `404 Not Found`: Curso não encontrada.


## Considerações de Segurança

[Discuta as considerações de segurança relevantes para a aplicação distribuída, como autenticação, autorização, proteção contra ataques, etc.]

## Implantação

[Instruções para implantar a aplicação distribuída em um ambiente de produção.]

1. Defina os requisitos de hardware e software necessários para implantar a aplicação em um ambiente de produção.
2. Escolha uma plataforma de hospedagem adequada, como um provedor de nuvem ou um servidor dedicado.
3. Configure o ambiente de implantação, incluindo a instalação de dependências e configuração de variáveis de ambiente.
4. Faça o deploy da aplicação no ambiente escolhido, seguindo as instruções específicas da plataforma de hospedagem.
5. Realize testes para garantir que a aplicação esteja funcionando corretamente no ambiente de produção.

## Testes

[Descreva a estratégia de teste, incluindo os tipos de teste a serem realizados (unitários, integração, carga, etc.) e as ferramentas a serem utilizadas.]

1. Crie casos de teste para cobrir todos os requisitos funcionais e não funcionais da aplicação.
2. Implemente testes unitários para testar unidades individuais de código, como funções e classes.
3. Realize testes de integração para verificar a interação correta entre os componentes da aplicação.
4. Execute testes de carga para avaliar o desempenho da aplicação sob carga significativa.
5. Utilize ferramentas de teste adequadas, como frameworks de teste e ferramentas de automação de teste, para agilizar o processo de teste.

# Referências

Inclua todas as referências (livros, artigos, sites, etc) utilizados no desenvolvimento do trabalho.
