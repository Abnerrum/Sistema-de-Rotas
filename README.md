🧭 Resumo Geral:
É um sistema completo para gerenciar rotas de técnicos de campo, ordens de serviço e cidades (com latitude e longitude pra integração com mapas).
Feito com React no frontend, Node.js + Express + tRPC no backend, e MySQL com Drizzle ORM.

⚙️ Estrutura:

Frontend (client/) → Interface feita em React 19 com Tailwind e Shadcn UI.

Backend (server/) → APIs criadas com tRPC, rodando no Express.

Banco (drizzle/) → Estrutura e migrações das tabelas MySQL.

🗂️ Principais Tabelas:

users: usuários do sistema (autenticação).

technicians: técnicos.

cities: cidades com latitude/longitude.

service_orders: ordens de serviço.

routes e route_items: rotas e os pontos (OS) dentro de cada rota.

💻 Funcionalidades Principais:

Cadastrar técnicos, cidades e produtos.

Gerar ordens de serviço com cliente, produto e defeito.

Criar rotas diárias para técnicos e atribuir OS a cada rota.

Acompanhar o status das rotas (planejamento → execução → concluída).

Visualizar mapa e sequência das visitas (baseado nas coordenadas).

📦 Tecnologias-Chave:

Frontend: React + Wouter + Tailwind + Shadcn

Backend: Express + tRPC + Zod

Banco: MySQL com Drizzle ORM

Autenticação: Manus OAuth
