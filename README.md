# Elias Rodrigues

**Engenheiro de Software · Backend** — Java · Spring Boot · Node.js · TypeScript · PostgreSQL

Bacharel em Ciência da Computação pela UFS. Construo APIs e sistemas que rodam em produção — regras de negócio, controle de acesso por papéis, consistência transacional e performance. Antes disso, dois anos de pesquisa em Machine Learning (PIBIC), com artigo publicado na ERBASE 2025.

**Disponível para início imediato em posições remotas de backend.**

[elias-costa.github.io](https://elias-costa.github.io/) · [LinkedIn](https://www.linkedin.com/in/elias-rodrigues-288450254/) · [ecrprofessional@gmail.com](mailto:ecrprofessional@gmail.com)

## Agora

Mantenho o **[SiteHealth](https://site-health-ten.vercel.app)**, um SaaS de monitoramento técnico de sites, no ar desde julho de 2026. Faz crawl periódico dos sites cadastrados e envia por e-mail um relatório priorizado do que afeta SEO e experiência do usuário: links e imagens quebrados, conteúdo misto, bloqueio acidental de indexação, certificado e domínio prestes a vencer.

É produto próprio — arquitetura, segurança e operação são decisões minhas: isolamento multi-tenant por RLS no banco, guarda de SSRF em todos os caminhos de saída, limite de taxa atômico no Postgres, 679 testes automatizados. O código é privado; o caso completo, com as decisões e a evidência de cada uma, está [no site](https://elias-costa.github.io/#sitehealth).

## Projetos

**[caixa-simples](https://github.com/Elias-Costa/caixa-simples)** — `Java 21 · Spring Boot 4 · Spring Modulith · PostgreSQL · Testcontainers`
PDV multi-tenant para pequenos negócios, construído como monolito modular. A fronteira entre os módulos é verificada por teste, cada tabela tem teste de isolamento entre contas, e a regra de negócio vive em classes sem Spring nem JPA. Em desenvolvimento.

**[som-ae](https://github.com/Elias-Costa/som-ae)** — `Python · PyTorch · NumPy`
Mapas auto-organizáveis em que cada neurônio é um autoencoder convolucional. Protótipo da pesquisa de Iniciação Científica; o artigo *Mapas Auto-Organizáveis e Autoencoders* saiu nos anais da ERBASE 2025, publicados pela SBC ([DOI](https://doi.org/10.5753/erbase.2025.13757)).

**Validação de conformidade com a LGPD** — `Node.js · TypeScript · PostgreSQL`
Sistema institucional da UFS, em produção. Desenvolvi as APIs, modelei o banco relacional e implementei regras de negócio alinhadas a requisitos legais. Código privado por lidar com dados sensíveis.

## Stack

| | |
|---|---|
| **Backend** | Java, Spring Boot, Node.js, TypeScript, Python, FastAPI, APIs REST |
| **Dados** | PostgreSQL, MongoDB, SQL, SQLAlchemy |
| **Segurança & arquitetura** | RBAC, autenticação JWT, Row Level Security, lógica transacional, arquitetura em camadas |
| **Infraestrutura** | Docker, Gradle, Git, Linux, AWS (EC2, S3, RDS), Vercel |
| **Machine Learning** | PyTorch, Scikit-learn |
