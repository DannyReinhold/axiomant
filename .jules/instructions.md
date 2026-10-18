# Axiomant Instructions & Architectural Guardrails

## 1. Vernac-First
- Axiomant's core domain and application logic must be implemented as fully as possible using the Vernac architecture language.
- Refer to `https://vernac.org` and specifically the Vernac AI reference (`ai-language-reference.md`) for syntax and conventions.
- Use the latest release version of Vernac and the Vernac Maven plugin (`0.5.0` or snapshot equivalent `0.5.0-SNAPSHOT` locally).
- Architecture follows strict DDD: IDs, Value Objects, Aggregates, transactional Usecases, Outbound Ports & Adapters, and durable Events. Target runtime is modern Java (Java 21+) and Spring Boot.

## 2. Strict 12-Factor App Compliance
- Configuration strictly via environment variables.
- Explicit dependency declarations.
- Stateless, disposable processes for horizontal scaling.
- Logs treated as event streams to stdout.

## 3. Explicit Vernac Feature Gap Escalation
- If a required system feature lacks a standard or idiomatic Vernac language abstraction, DO NOT create arbitrary ad-hoc workarounds.
- Explicitly document this in a dedicated section in `ARCHITECTURAL_GAPS.md` so that standard language support can be designed directly into the Vernac project or a dedicated extension library.

## 4. Coding Standards
- Follow standard Spring Boot and Java 21 conventions for anything not covered by Vernac.
- Keep tests and core logic isolated appropriately.
