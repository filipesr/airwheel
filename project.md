
## 🧩 Visão Geral do Projeto

**Produto:** Venda de itens online com fluxo distinto de **pagamento, frete e estoque** por país.
**Mercados-alvo:** Brasil e Paraguai
**Tecnologias principais:**

* **Frontend:** Next.js + TailwindCSS
* **Backend:** Node.js (Express.js ou Fastify)
* **Banco de Dados:** MongoDB (Atlas)
* **Autenticação:** JWT + Auth Provider (Google/Email)
* **Pagamentos:**

  * Brasil: Mercado Pago / Pix
  * Paraguai: Bancard / Pagopar
* **Infra:** Vercel (frontend), Railway/Fly.io/Render (backend), MongoDB Atlas

---

## 🏗️ Estrutura Separada dos E-commerces

Cada país terá:

* URL separada (`.com.br`, `.com.py`)
* Painel de administração próprio
* Gateway de pagamento exclusivo
* Política de frete e impostos específica
* Catálogo sincronizado, com estoque separado ou centralizado

---

## 🧑‍💻 Equipe Recomendada

| Função                  | Quantidade | Perfil                                     |
| ----------------------- | ---------- | ------------------------------------------ |
| Product Owner           | 1          | Visão do negócio, validação e testes       |
| Desenvolvedor Fullstack | 2–4        | Node.js + Next.js + MongoDB                |
| UI/UX Designer          | 1          | Baseado na Airwheel.ph                     |
| QA/Tester               | 1          | Testes manuais e automatizados             |
| DevOps (opcional)       | 1          | CI/CD, monitoramento e deploy automatizado |

---

## 🕒 Cronograma e Carga de Trabalho

### 1. Desenvolvimento Normal (5–6 semanas por e-commerce)

| Etapa                           | Tempo Estimado (dias úteis)     | Recursos Envolvidos |
| ------------------------------- | ------------------------------- | ------------------- |
| Levantamento de Requisitos      | 2                               | PO + Dev + Designer |
| Design (UX/UI)                  | 5                               | Designer            |
| Configuração de infraestrutura  | 2                               | Dev + DevOps        |
| Backend (API REST + Admin)      | 8                               | Fullstack Dev       |
| Frontend (Público + Responsivo) | 6                               | Fullstack Dev       |
| Integração de pagamentos        | 3                               | Fullstack Dev       |
| Testes + QA                     | 3                               | QA                  |
| Ajustes finais + Deploy         | 2                               | Todos               |
| **Total estimado (por país)**   | **29 dias úteis (\~6 semanas)** |                     |

---

### 2. Desenvolvimento Acelerado (2 semanas por e-commerce)

Para entrega em 10 dias úteis será necessário:

* Reduzir escopo (MVP puro)
* Aumentar equipe (4 devs em paralelo)

| Etapa                                  | Tempo Estimado (dias úteis) |
| -------------------------------------- | --------------------------- |
| Design Rápido (baseado em Airwheel.ph) | 1                           |
| Infraestrutura pronta no dia 1         | 1                           |
| Backend + Frontend simultâneos         | 6                           |
| Integrações e testes                   | 2                           |
| Ajustes + deploy                       | 1                           |
| **Total estimado (por país)**          | **10 dias úteis**           |

---

## 💸 Estimativa de Custos (por projeto / por país)

### 💼 Mão de Obra (freelancers ou equipe interna)

| Cargo               | Faixa de Custo (R\$)  | Tempo estimado |
| ------------------- | --------------------- | -------------- |
| Fullstack Dev       | R\$ 8.000–14.000      | 6 semanas      |
| UI/UX Designer      | R\$ 3.000–5.000       | 1 semana       |
| QA                  | R\$ 2.000–4.000       | 1 semana       |
| PO ou Consultor     | R\$ 3.000–5.000       | Parcial        |
| **Total Normal**    | **R\$ 16.000–28.000** |                |
| **Total Acelerado** | **R\$ 30.000–45.000** | + equipe extra |

---

## 🔩 Recursos Técnicos

| Recurso                        | Plano sugerido          | Custo mensal (estimado)    |
| ------------------------------ | ----------------------- | -------------------------- |
| MongoDB Atlas                  | Shared ou M10 cluster   | R\$ 0–150                  |
| Vercel (frontend hosting)      | Free ou Pro             | R\$ 0–100                  |
| Backend (Railway/Fly.io)       | Free até certo ponto    | R\$ 0–150                  |
| Domínios `.com.br` / `.com.py` | Registro.br + NIC       | R\$ 40/ano + intermediário |
| CDN / Imagens (Cloudinary)     | Free tier ou Pro        | R\$ 0–50                   |
| Email (Resets, transações)     | Resend / Mailgun / SMTP | R\$ 0–40                   |
| Monitoramento (Uptime, logs)   | Logtail / Sentry        | R\$ 0–60                   |

---

## 🧩 MVP Recomendado

* Catálogo (produtos, imagens, preços)
* Carrinho + checkout
* Cadastro/Login
* Admin básico com gerenciamento de produtos e pedidos
* Integração com gateway de pagamento local
* Frete fixo ou por API dos Correios (Brasil) / Local (PY)
* Layout responsivo com visual Airwheel.ph

