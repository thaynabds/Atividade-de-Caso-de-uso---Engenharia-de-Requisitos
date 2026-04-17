# Atividade-de-Caso-de-uso---Engenharia-de-Requisitos
# Atividade — Diagrama de Caso de Uso

**Aluna:** Thayná Batista da Silva  
**Disciplina:** ENGENHARIA DE REQUISITOS - 2026.1
**Instituição:** Faculdade Senac  
**Ferramenta utilizada:** [Lucid.app](https://lucid.app/)

---

## Atividade 1 — Sistema de Reservas de Mesas para Restaurante

O sistema permite que clientes façam reservas e que funcionários gerenciem essas reservas e as mesas do restaurante.

**Atores:** Cliente, Funcionário

| Caso de Uso | Ator(es) |
|---|---|
| Fazer Reserva | Cliente |
| Cancelar Reserva *(prazo 24h)* | Cliente |
| Atualizar Reserva | Cliente |
| Visualizar Reservas | Cliente, Funcionário |
| Gerenciar Mesas | Funcionário |

---

## Atividade 2 — Sistema de Biblioteca Online

O sistema modela as funcionalidades essenciais de uma biblioteca digital.

**Atores:** Membro da Biblioteca, Bibliotecário

| Caso de Uso | Ator(es) | Relação |
|---|---|---|
| Pesquisar Livro | Membro da Biblioteca | — |
| Realizar Empréstimo | Membro da Biblioteca | `<<include>>` Verificar Débitos |
| Devolver Livro | Membro da Biblioteca | `<<include>>` Verificar Débitos |
| Verificar Débitos | — | Incluído por Empréstimo e Devolução |
| Cadastrar Livro | Bibliotecário | Exclusivo |

**Justificativa do `<<include>>`:** Tanto "Realizar Empréstimo" quanto "Devolver Livro" obrigatoriamente verificam se o membro possui débitos pendentes antes de concluir a operação. Por isso, ambos incluem o caso de uso "Verificar Débitos".

---

## Como visualizar os diagramas

Os diagramas foram criados no [Lucid.app](https://lucid.app/). Para acessar:

1. Acesse [lucid.app](https://lucid.app/) e faça login.
2. Crie um novo documento e selecione **UML Diagram**.
3. Utilize as formas de **Use Case Diagram** (elipses para casos de uso, stickman para atores e retângulo de limite de sistema).
4. Para o relacionamento `<<include>>`, use uma seta tracejada com o estereótipo `<<include>>` apontando do caso de uso base para o incluído.

