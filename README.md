# 🏬 TechStore – Migração de Arquitetura Monolítica para Microsserviços

Documentação técnica do projeto desenvolvido para a disciplina **Projeto Integrador III-A** da **PUC Goiás (EAD)**.  
O objetivo é apresentar a proposta completa de modernização da arquitetura da empresa fictícia **TechStore**, migrando de um monólito para uma estrutura baseada em *microservices*.

---

## 📌 Objetivo do Projeto

Transformar uma aplicação monolítica em uma arquitetura distribuída, focando em:

- 🔹 Escalabilidade  
- 🔹 Segurança da informação  
- 🔹 Resiliência  
- 🔹 Melhor desempenho  
- 🔹 Maior autonomia entre equipes  

---

## 🎯 Objetivos Específicos

- Analisar limitações do sistema atual;  
- Definir os microsserviços e suas responsabilidades;  
- Criar uma estratégia de migração segura e progressiva;  
- Documentar mecanismos de segurança (CID);  
- Apresentar diagramas e justificativas técnicas.

---

## 🏛️ Arquitetura Atual — Monolito

Atualmente, a TechStore possui um sistema único contendo:

- Autenticação  
- Catálogo de produtos  
- Pedidos  
- Pagamentos  

### ❗ Principais problemas:

- Baixa escalabilidade  
- Deploy complexo  
- Alta dependência tecnológica  
- Risco elevado de queda geral  

---

## 🚀 Por que migrar?

- Deploy mais rápido  
- Melhor desempenho sob carga  
- Redução de falhas sistêmicas  
- Maior flexibilidade tecnológica  
- Rastreabilidade e segurança aprimoradas  

---

## 🧩 Microsserviços Propostos

| Service              | Responsibilities            | Technology    | Database   |
| -------------------- | --------------------------- | ------------- | ---------- |
| Auth Service         | JWT, login, roles           | Java + Spring | PostgreSQL |
| Product Service      | Products, stock, categories | Java + Spring | MongoDB    |
| Order Service        | Orders, history             | Java + Spring | PostgreSQL |
| Payment Service      | Payment processing          | Java + Spring | MySQL      |
| Notification Service | E-mails, alerts             | MQ Worker     | Redis      |

---

## 🛣️ Estratégia de Migração

1️⃣ Criar Auth e Products paralelamente ao monólito  
2️⃣ Implementar API Gateway  
3️⃣ Migrar Pedidos e Pagamentos  
4️⃣ Desativar módulo por módulo do monólito  
5️⃣ Containerizar tudo com Docker + Kubernetes  

---

## 🔐 Segurança (CID)

| Pillar          | Mechanism       | Purpose                      |
| --------------- | --------------- | ---------------------------- |
| Confidentiality | TLS, JWT        | Protect sensitive data       |
| Integrity       | Logging, HMAC   | Prevent unauthorized changes |
| Availability    | Replication, LB | Ensure system uptime         |

---

## 📝 Conclusão

A migração trará ganhos expressivos em:

- Velocidade de desenvolvimento  
- Estabilidade  
- Segurança  
- Escalabilidade  
- Independência entre equipes  

O projeto demonstra como uma arquitetura moderna melhora a eficiência geral da TechStore.

---

## 📚 Referências

- Newman, S. *Building Microservices*. O'Reilly.  
- Richardson, C. *Microservices Patterns*. Manning.  
- Fowler, M. *Monolith to Microservices*. O'Reilly.  
- ISO/IEC 27001:2013.

---

## 👥 Autores

- João Vitor Ferreira da Silva  
- Pedro Nunes Marques Junior  
- Victor Hugo Batista Pereira  
- Ariel Jorge da Silva  
- Leandro Batista de Sousa Galdido  

---

## 📍 Instituição

**PUC Goiás – EAD**  
**Curso:** Análise e Desenvolvimento de Software  
**Disciplina:** Projeto Integrador III-A  
**Professor:** José Ricardo Cosme Lerias Ribeiro  
**Cidade:** Goiânia  
**Data:** 01/11/2025 
