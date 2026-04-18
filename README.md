# Atividade-de-Caso-de-uso---Engenharia-de-Requisitos
# Atividade — Diagrama de Caso de Uso
**Aluna:** Thayná Batista da Silva  
**Disciplina:** ENGENHARIA DE REQUISITOS - 2026.1  
**Instituição:** Faculdade Senac  
**Ferramenta utilizada:** [Miro](https://miro.com/app/board/uXjVGxJsrAY=/?share_link_id=890481171226)
 
---
 
Documentação dos diagramas desenvolvidos como atividade prática de modelagem UML, cobrindo dois sistemas distintos.
 
---
 
## 📁 Estrutura do Projeto
 
```
Atividade-de-Caso-de-uso---Engenharia-de-Requisitos/
├── README.md
└── diagramas/
    ├── diagrama-reserva-mesas.png
    └── diagrama-biblioteca-online.png
```
 
🔗 **Board no Miro:** [Acessar diagrama](https://miro.com/app/board/uXjVGxJsrAY=/?share_link_id=890481171226)
 
---
 
## 🍽️ Sistema de Reserva de Mesas
 
### Descrição
Modela as funcionalidades de um restaurante que permite a clientes fazerem reservas de mesas e a funcionários gerenciarem essas reservas.
 
### Atores
 
| Ator | Descrição |
|---|---|
| **Cliente** | Realiza, cancela e atualiza reservas |
| **Funcionário** | Gerencia reservas e mesas do restaurante |
 
### Casos de Uso
 
| Caso de Uso | Ator Responsável | Observação |
|---|---|---|
| Fazer Reserva | Cliente | — |
| Cancelar Reserva | Cliente | Prazo máximo de 24h |
| Atualizar Reserva | Cliente | — |
| Visualizar Reservas | Funcionário | — |
| Gerenciar Mesas | Funcionário | — |
 
### Guia de Cores (Miro)
 
- 🔵 **Azul escuro** — Casos de uso do Cliente
- 🟢 **Verde** — Casos de uso do Funcionário
- **Ator preto** — Cliente
- **Ator azul** — Funcionário
---
 
## 📚 Sistema de Biblioteca Online
 
### Descrição
Modela as funcionalidades essenciais de uma biblioteca digital, incluindo empréstimos, devoluções, pesquisa de livros e cadastro de acervo.
 
### Atores
 
| Ator | Descrição |
|---|---|
| **Membro da Biblioteca** | Pesquisa livros, realiza empréstimos e devoluções |
| **Bibliotecário** | Gerencia o acervo cadastrando novos livros |
 
### Casos de Uso
 
| Caso de Uso | Ator Responsável | Tipo |
|---|---|---|
| Pesquisar Livro | Membro da Biblioteca | Base |
| Realizar Empréstimo | Membro da Biblioteca | Base |
| Devolver Livro | Membro da Biblioteca | Base |
| Verificar Débitos | — | `<<extend>>` |
| Cadastrar Livro | Bibliotecário | Base (exclusivo) |
 
### Relações `<<extend>>`
 
> **Regra UML:** a seta tracejada parte **sempre** do caso estendido (comportamento extra) e aponta para o caso base.
 
```
Verificar Débitos ──<<extend>>──▶ Realizar Empréstimo
Verificar Débitos ──<<extend>>──▶ Devolver Livro
```
 
"Verificar Débitos" é um comportamento opcional/extra que pode ocorrer durante um empréstimo ou devolução. Por isso ele **estende** os dois casos base.
 
### Guia de Cores (Miro)
 
- 🔵 **Azul** — Casos de uso do Membro da Biblioteca
- 🟠 **Laranja** — Caso de uso `<<extend>>` (Verificar Débitos)
- 🟢 **Verde** — Caso de uso exclusivo do Bibliotecário (Cadastrar Livro)
- **Ator azul** — Membro da Biblioteca
- **Ator vermelho** — Bibliotecário
- **Seta sólida** — Associação (ator → caso de uso)
- **Seta tracejada laranja** — Relação `<<extend>>`
---
 
## 📌 Conceitos UML Utilizados
 
### Fronteira do Sistema (System Boundary)
Retângulo que delimita o escopo do sistema. Casos de uso ficam dentro; atores ficam fora.
 
### Associação
Linha sólida entre um ator e um caso de uso. Indica que o ator participa daquele fluxo.
 
### `<<extend>>`
Relação entre casos de uso onde um comportamento **opcional ou condicional** estende um caso base.
A seta tracejada aponta **do caso extra para o caso base**.
 
### `<<include>>`
Relação onde um caso de uso **obrigatoriamente inclui** outro (não utilizado neste projeto).
 
---
 
## ✅ Checklist de Validação
 
### Reserva de Mesas
- [x] Cliente conectado a: Fazer Reserva, Cancelar Reserva, Atualizar Reserva
- [x] Funcionário conectado a: Visualizar Reservas, Gerenciar Mesas
- [x] "Visualizar Reservas" escrito corretamente (sem erro de digitação)
- [x] Nenhum ator com associação indevida
### Biblioteca Online
- [x] Membro conectado a: Pesquisar Livro, Realizar Empréstimo, Devolver Livro
- [x] Bibliotecário conectado apenas a: Cadastrar Livro
- [x] `<<extend>>`: Verificar Débitos → Realizar Empréstimo
- [x] `<<extend>>`: Verificar Débitos → Devolver Livro
- [x] Setas tracejadas na direção correta (do caso extra para o base)
- [x] Rótulo `<<extend>>` visível sobre cada seta
---
 
## 👩‍🎓 Autora
 
| Nome | Instituição | Disciplina |
|---|---|---|
| Thayná Batista da Silva | Faculdade Senac | Engenharia de Requisitos — 2026.1 |
 
---
 
*Atividade prática de modelagem UML — Diagramas de Caso de Uso*
 
