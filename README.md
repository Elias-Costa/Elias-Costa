# Elias Rodrigues

**Engenheiro de Software** · Backend, sistemas transacionais e aplicações offline.

Desenvolvo e mantenho produtos da modelagem do domínio à implantação, com foco em consistência de dados, segurança e recuperação de falhas. Minha base é backend; também construo as interfaces e cuido da operação dos produtos próprios.

Bacharel em Ciência da Computação pela UFS, com experiência em sistemas institucionais e dois anos de pesquisa em Machine Learning.

**Disponível para início imediato em posições remotas de Engenharia de Software.**

[Portfólio](https://elias-costa.github.io/) · [LinkedIn](https://www.linkedin.com/in/elias-rodrigues-288450254/) · [E-mail](mailto:ecrprofessional@gmail.com)

## Projetos em destaque

### [ECRX Caixa](https://caixa.ecrxtecnologia.com.br/)

Sistema de caixa e vendas para pequenos negócios. Reúne vendas, caixa, estoque, fiado e relatórios, com PWA que permite continuar o atendimento sem internet. Cuido do produto, da modelagem de domínio, do backend, da interface e da operação.

- **Monolito modular:** Java, Spring Boot e Spring Modulith, com domínio independente de framework e fronteiras verificadas por teste.
- **Sincronização idempotente:** operações nascem no aparelho; o servidor grava o resultado na mesma transação do efeito, permitindo reenvio após perda da resposta.
- **Pix com dois provedores:** Efí e Inter atrás de uma interface única, escolhida por Conta; o servidor reconsulta a cobrança no provedor antes de confirmar o pagamento.
- **Dados e acesso:** PostgreSQL, isolamento entre contas e autorização por perfil, com mais de 900 testes automatizados e os de banco contra PostgreSQL real, via Testcontainers.
- **Operação própria:** VPS no Brasil, Docker, CI no GitHub Actions, monitoramento e backups horários do PostgreSQL, cifrados antes do envio ao **Amazon S3**, com restauração ensaiada. O resumo de cada caixa fechado vai por e-mail pelo **Amazon SES**, por um outbox que impede uma falha no envio de desfazer o fechamento.

**Estado:** implantado e em preparação para o piloto, por enquanto só com contas de teste. O Pix integrado já foi exercitado no ambiente de testes do Inter; a Efí ainda aguarda as credenciais de homologação.

[Produto no ar](https://caixa.ecrxtecnologia.com.br/) · [Código](https://github.com/Elias-Costa/ecrx-caixa)

### Fichinhas

PWA de fiado e estoque construído para uma revendedora de cosméticos, com uso real. Organiza fichas, vendas, parcelas e recebimentos; evoluiu com estoque integrado às vendas, fotos, catálogo PDF para compartilhar no WhatsApp e um resumo com o que há a receber, o lucro do mês e os produtos encalhados.

React, TypeScript e Dexie/IndexedDB no aparelho; Supabase/PostgreSQL na nuvem. Registro e fila são gravados na mesma transação local, com identidade gerada no dispositivo. Dinheiro é `bigint` de centavos, correções preservam o histórico e as invariantes financeiras também valem no banco.

**Estado:** fichas, fiado e estoque em uso real. Gastos, cópia completa, textos editáveis, lembretes, a cópia diária no Google Drive e o Resumo chegaram em novembro e já foram conferidos no aparelho.

[Código](https://github.com/Elias-Costa/controle-estoque-gastos)

### [SiteHealth](https://site-health-ten.vercel.app)

SaaS de monitoramento técnico de sites. Faz varreduras periódicas e envia relatórios priorizados por e-mail sobre problemas que afetam SEO e experiência do usuário.

Next.js, TypeScript, Supabase, Inngest, Resend e Sentry. O trabalho de engenharia inclui processamento assíncrono em lotes com checkpoint, isolamento por RLS, proteção de SSRF e limites de taxa atômicos no PostgreSQL, com validação em sites reais.

**Estado:** no ar, em pré-lançamento, com cobrança em modo de teste. Código privado; posso apresentar a arquitetura em conversa técnica.

[Produto no ar](https://site-health-ten.vercel.app)

## Outros projetos

### [invoice-microservices](https://github.com/Elias-Costa/invoice-microservices)

Fechamento de notas fiscais internas em microsserviços. Estoque e faturamento têm cada um seu banco, e o fechamento da nota é uma Saga por eventos no Kafka: o faturamento pede a baixa, e a nota fecha quando o estoque confirma ou volta a ficar aberta, com o motivo, se faltar saldo.

Java 21, Spring Boot 4, Spring Cloud Gateway, Apache Kafka, PostgreSQL e frontend Angular 22, tudo em Docker Compose. Outbox transacional, idempotência HTTP por `Idempotency-Key`, consumidor que não reprocessa e bloqueio otimista no saldo, com 399 testes no backend, 124 deles de integração contra PostgreSQL e Kafka reais via Testcontainers, e as fronteiras da arquitetura hexagonal verificadas com ArchUnit.

**Estado:** `v0.1.0` publicada como demonstração local, com cinco roteiros automatizados (fluxo feliz, saldo insuficiente, concorrência, idempotência e queda do estoque). Sem login e sem integração com a SEFAZ.

[Código](https://github.com/Elias-Costa/invoice-microservices)

## Experiência e pesquisa

- **SergipeTec — Desenvolvedor Backend** · Estágio, mai–jul/2026. APIs em Java/Spring Boot, regras transacionais e otimização de endpoints de 8 s para 300 ms.
- **STI/UFS — Desenvolvedor Backend** · abr/2025–fev/2026. APIs em Node.js/TypeScript, modelagem PostgreSQL e regras de negócio do **LGPDefender**, sistema institucional de inventários de dados pessoais. Sou coautor do software, registrado no INPI (BR512026006717-0).
- **UFS — Iniciação Científica (PIBIC)** · set/2023–set/2025. Modelos e experimentação em Machine Learning com PyTorch. Coautor de *Mapas Auto-Organizáveis e Autoencoders*, publicado na ERBASE 2025 pela SBC. [Artigo](https://doi.org/10.5753/erbase.2025.13757) · [Código SOM-AE](https://github.com/Elias-Costa/som-ae).

## Stack e práticas

| Área | Tecnologias e práticas |
|---|---|
| **Backend e dados** | Java, Spring Boot, Spring Data JPA/Hibernate, Spring Security, Spring Cloud Gateway, Node.js, TypeScript, Python, APIs REST, PostgreSQL, SQL, Flyway, Supabase |
| **Arquitetura e confiabilidade** | Modelagem de domínio, monolito modular, Spring Modulith, arquitetura hexagonal, microsserviços, Apache Kafka, Saga, outbox transacional, consistência transacional, idempotência, offline-first |
| **Segurança** | RBAC, autenticação JWT, Row Level Security, isolamento entre contas |
| **Interface e PWA** | React, Angular, Next.js, Tailwind CSS, Vite, service worker, IndexedDB, Dexie, HTML/CSS |
| **Testes** | JUnit, Mockito, Testcontainers, ArchUnit, Bun Test, Vitest, Playwright, integração contra banco real |
| **Operação** | Docker, Docker Compose, Maven, GitHub Actions, Git, Linux, VPS, AWS (EC2, RDS), **Amazon S3 (backups cifrados)**, Amazon SES, Vercel, backup e restauração |
| **Machine Learning** | PyTorch, Scikit-learn, experimentação |
