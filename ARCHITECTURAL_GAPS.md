# Architectural Gaps & Feature Requests

This document tracks system requirements that cannot currently be implemented using standard Vernac (`0.5.0` / `0.5.0-SNAPSHOT`) abstractions.

If you encounter such a requirement, document it here instead of creating ad-hoc framework workarounds. This allows proper abstraction design in the Vernac project.

## Template:
### [Feature Name]
- **Description**: Brief explanation of the required functionality.
- **Why it's needed**: Context in Axiomant.
- **Current Limitation in Vernac**: Why Vernac doesn't support this out of the box (with references to current rules).
- **Proposed/Requested Language Extension**: Idea for how it could look in Vernac syntax.

---

### Endpoints Without Built-in Vernac Abstractions
- **Description**: Certain complex or specialized HTTP inbound endpoints might fall outside the declarative scope.
- **Why it's needed**: Webhooks or specific binary handling.
- **Current Limitation in Vernac**: `adapter ... inbound http` currently has defined constraints.
- **Proposed/Requested Language Extension**: Open for investigation.
