# Case studies

Notas de ingeniería sobre los dos sistemas que he construido. El código es privado —uno es producto propio en desarrollo, el otro contiene estrategia propia— así que aquí publico lo que sí se puede revisar sin exponerlo: la arquitectura, las decisiones y los errores que costaron algo.

Cada documento responde tres preguntas: qué se construyó, qué decisiones lo sostienen y qué haría distinto.

| Caso | Stack | Qué muestra |
|---|---|---|
| [LuckAgents — SaaS multi-tenant de agentes de IA](luckai-saas-multitenant.md) | TypeScript · Node/Express · React · Next.js · PostgreSQL/Supabase · MongoDB · Redis · Docker | Aislamiento entre clientes en la base de datos, idempotencia en efectos externos, y una auditoría que terminó en NO-GO para producción con la suite en verde |
| [Plataforma cuantitativa para mercados electrónicos](plataforma-cuantitativa.md) | Rust (Tokio) · Python · Polars · DuckDB · Parquet · XGBoost/CatBoost/LightGBM | Aritmética decimal en rutas de dinero, paridad Python↔Rust como contrato, y controles de validación que se prueban fallando |

Sin cifras de negocio, sin resultados financieros, sin credenciales, sin datos de clientes. Donde una decisión dependía de información que no me corresponde publicar, está descrita por su forma y no por su contenido.

## Código que acompaña estas notas

Una de las decisiones del primer caso está publicada como implementación ejecutable, no solo descrita:

**[multi-tenant-rls](https://github.com/joshua-angulo/multi-tenant-rls)** — el aislamiento entre clientes con Row Level Security, en ~200 líneas de SQL y TypeScript, con 16 pruebas en su mayoría negativas y una verificación por mutación que comprueba que la suite detecta su propio fallo. Se corre en dos minutos.

Puedo recorrer el resto del código y la arquitectura completa en una entrevista.

**Joshua Angulo González** — Software Engineer · Culiacán, Sinaloa, México
[linkedin.com/in/joshuaangulogonzalez](https://www.linkedin.com/in/joshuaangulogonzalez/) · [joshuaangulo10@gmail.com](mailto:joshuaangulo10@gmail.com)

---

**In English.** Engineering notes on the two systems I've built. The code is private — one is a product in development, the other holds proprietary strategy — so what's published here is what can be reviewed without exposing it: architecture, decisions, and the mistakes that cost something. No business figures, no financial results, no credentials, no customer data.
