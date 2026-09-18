# Elias Rodrigues

**Engenheiro de Software · Full Stack** — Java · Spring Boot · TypeScript · Node.js · React · PostgreSQL

Bacharel em Ciência da Computação pela UFS. Construo produtos completos que rodam em produção — da modelagem do banco e das regras de negócio à interface que o usuário toca. Minha base é backend: controle de acesso por papéis, consistência transacional, performance. O frontend veio pelos produtos próprios, em React e Next.js, e hoje faz parte do que entrego de ponta a ponta. Antes disso, dois anos de pesquisa em Machine Learning (PIBIC), com artigo publicado na ERBASE 2025.

**Disponível para início imediato em posições remotas full stack ou backend.**

[elias-costa.github.io](https://elias-costa.github.io/) · [LinkedIn](https://www.linkedin.com/in/elias-rodrigues-288450254/) · [ecrprofessional@gmail.com](mailto:ecrprofessional@gmail.com)

## Agora

Mantenho o **[SiteHealth](https://site-health-ten.vercel.app)**, um SaaS de monitoramento técnico de sites, no ar desde julho de 2026. Faz crawl periódico dos sites cadastrados e envia por e-mail um relatório priorizado do que afeta SEO e experiência do usuário: links e imagens quebrados, conteúdo misto, bloqueio acidental de indexação, certificado e domínio prestes a vencer.

É produto próprio, do banco à tela — arquitetura, segurança, interface e operação são decisões minhas: Next.js e React no front, isolamento multi-tenant por RLS no banco, guarda de SSRF em todos os caminhos de saída, limite de taxa atômico no Postgres, 679 testes automatizados. O código é privado; o caso completo, com as decisões e a evidência de cada uma, está [no site](https://elias-costa.github.io/#sitehealth).

## Projetos

**[caixa-simples](https://github.com/Elias-Costa/caixa-simples)** — `Java 21 · Spring Boot 4 · Spring Modulith · PostgreSQL · Testcontainers`
PDV multi-tenant para pequenos negócios, construído como monolito modular. A fronteira entre os módulos é verificada por teste, cada tabela tem teste de isolamento entre contas, e a regra de negócio vive em classes sem Spring nem JPA. Em desenvolvimento.

**[invoice-microservices](https://github.com/Elias-Costa/invoice-microservices)** — `Java 21 · Spring Boot 4 · Apache Kafka · PostgreSQL · Testcontainers · Docker Compose`
Emissão de notas fiscais em microsserviços: um banco por serviço, consulta síncrona entre eles e toda mudança de estado por evento, com Saga coordenada por outbox. Comecei pela fundação compartilhada — erros em Problem Details (RFC 9457), idempotência HTTP por `Idempotency-Key`, transactional outbox e guarda contra evento reprocessado no consumidor — cada peça provada contra Postgres e Kafka reais via Testcontainers. Cada decisão está registrada em ADR ou num log numerado. Em desenvolvimento; os serviços de estoque e faturamento e o frontend em Angular vêm em seguida.

**[controle-estoque-gastos](https://github.com/Elias-Costa/controle-estoque-gastos)** — `TypeScript · React · Tailwind · PWA · Supabase (Postgres + RLS) · Dexie · Bun · Playwright`
PWA offline-first que substitui o caderno de fiado de quem revende cosméticos por conta própria. Toda escrita vai primeiro ao banco local do aparelho e sobe por uma fila com ids UUIDv7 gerados no dispositivo, o que torna o reenvio idempotente por construção; lançamento financeiro é imutável (correção é estorno) e dinheiro é `bigint` de centavos. As invariantes financeiras e o isolamento por conta valem no próprio Postgres, e uma suíte tenta violá-las contornando o app. As telas foram desenhadas contra um protótipo cronometrado, para o celular, e provadas em iPhone real e no Chromium contra o build de produção: venda sem rede que sobrevive a recarregar, reenvio que não duplica, dois aparelhos que convergem. Fase 1 (fichas, fiado e cobrança) pronta.

**[som-ae](https://github.com/Elias-Costa/som-ae)** — `Python · PyTorch · NumPy`
Mapas auto-organizáveis em que cada neurônio é um autoencoder convolucional. Protótipo da pesquisa de Iniciação Científica; o artigo *Mapas Auto-Organizáveis e Autoencoders* saiu nos anais da ERBASE 2025, publicados pela SBC ([DOI](https://doi.org/10.5753/erbase.2025.13757)).

**Validação de conformidade com a LGPD** — `Node.js · TypeScript · PostgreSQL`
Sistema institucional da UFS, em produção. Desenvolvi as APIs, modelei o banco relacional e implementei regras de negócio alinhadas a requisitos legais. Código privado por lidar com dados sensíveis.

## Stack

| | |
|---|---|
| **Backend** | Java, Spring Boot, Node.js, TypeScript, Python, FastAPI, APIs REST, Apache Kafka |
| **Frontend** | React, Next.js, Tailwind CSS, Vite, PWA (service worker, IndexedDB), HTML/CSS |
| **Dados** | PostgreSQL, MongoDB, SQL, SQLAlchemy, Supabase |
| **Segurança & arquitetura** | RBAC, autenticação JWT, Row Level Security, lógica transacional, arquitetura em camadas, monolito modular, microsserviços, idempotência, transactional outbox, offline-first |
| **Testes** | JUnit, Testcontainers, Vitest, Playwright, testes de integração contra banco real |
| **Infraestrutura** | Docker, Docker Compose, Gradle, Maven, Git, Linux, AWS (EC2, S3, RDS), Vercel |
| **Machine Learning** | PyTorch, Scikit-learn |
