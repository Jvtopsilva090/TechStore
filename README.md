🏬 TechStore – Microservices Migration Architecture

<p align="center">








</p>
📘 Overview

This repository documents the migration of the TechStore system from a monolithic structure to a modern microservices architecture focused on scalability, resilience, and security.

A detailed proposal and technical documentation were created as part of the Projeto Integrador III-A (PUC Goiás - EAD).

🗂️ Repository Structure
/
├── docs/
│   ├── architecture.md
│   ├── security.md
│   ├── migration-plan.md
│   └── diagrams/
│       ├── high-level-architecture.png
│       └── microservices-flow.png
├── README.md
└── Projeto_TechStore.pdf

🧩 Microservices Overview
Service	Responsibilities	Tech	Database
Auth Service	JWT, login, roles	Java + Spring	PostgreSQL
Product Service	Products, stock, categories	Java + Spring	MongoDB
Order Service	Orders, history	Java + Spring	PostgreSQL
Payment Service	Gateway integration	Java + Spring	MySQL
Notification Service	Emails, alerts	MQ Worker	Redis
🏗️ High-Level Architecture Diagram
                           ┌─────────────────────────────┐
                           │         API Gateway          │
                           └──────────────┬──────────────┘
                                          │
         ┌────────────────────────────────┼──────────────────────────────────┐
         │                                │                                  │
┌──────────────────┐          ┌──────────────────┐               ┌──────────────────┐
│   Auth Service    │          │ Product Service  │               │  Order Service   │
└──────────────────┘          └──────────────────┘               └──────────────────┘
         │                                │                                  │
         ▼                                ▼                                  ▼
 PostgreSQL                        MongoDB                        PostgreSQL

         ┌────────────────────────────────┼──────────────────────────────────┐
         │                                │                                  │
┌──────────────────┐          ┌──────────────────┐               ┌──────────────────┐
│ Payment Service   │          │ Notification Svc │               │ Message Broker   │
└──────────────────┘          └──────────────────┘               └──────────────────┘
         │                                │                                  │
         ▼                                ▼                                  ▼
      MySQL                             Redis                           RabbitMQ

🔐 Security Model (CID)
Pillar	Mechanism	Goal
Confidentiality	TLS + JWT	Protect sensitive data
Integrity	Logs + HMAC	Ensure data consistency
Availability	Replication + LB	Keep services online
🌍 English Summary

The TechStore platform is being modernized using a microservices architecture.
This transition enhances:

Scalability

Deployment agility

Security

Fault isolation

Maintainability

Each domain of the system becomes an independent service, communicating through REST APIs and message queues (RabbitMQ).

👥 Authors

João Vitor Ferreira da Silva

Pedro Nunes Marques Junior

Victor Hugo Batista Pereira

Ariel Jorge da Silva

Leandro Batista de Sousa Galdido

🎓 Academic Information

PUC Goiás – EAD
Course: Análise e Desenvolvimento de Software
Discipline: Projeto Integrador III-A
Professor: José Ricardo Cosme Lerias Ribeiro
Date: 01/11/2025

📄 License

This project is distributed under the MIT License.
