# Frequently Asked Questions

## How do you secure customer environments?

CheckID is delivered as a managed SaaS service with customer-specific isolation. Each customer is onboarded with dedicated configuration and tenant-scoped access controls. Secrets and certificates are stored in Azure Key Vault, service-to-service access uses managed identities and traffic/data are protected with encryption in transit and at rest. We continuously monitor service health and security telemetry to detect and respond to issues quickly.

## How do you handle PII?

CheckID processes only the minimum identity attributes required to complete authentication and TAP creation, and does so transiently in-memory. We do not store, retain, or log personal data in CheckID.

The customer remains the Data Controller; identity records remain in the customer’s Entra ID.

## Who has access to CheckID Platform?

Access is restricted to authorized personnel only and is governed by Microsoft Entra ID, role-based access control, and privileged access workflows (PIM). Only approved administrators/operators can manage configuration, and access is controlled through auditable role assignments and least-privilege principles.

## If an issues occurs, how will you notify us?

We use proactive monitoring and alerting (including health checks and telemetry) to detect service issues early. If an incident occurs, we follow defined incident-response processes and notify through agreed support channels such as email, ticketing, and optional Teams escalation, with critical incidents acknowledged within one business day.
