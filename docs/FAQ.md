# Frequently Asked Questions

## How do you secure customer environments?

CheckID is delivered as a managed SaaS service with customer-specific isolation. Each customer is onboarded with dedicated configuration and tenant-scoped access controls. Secrets and certificates are stored in Key Vault, service-to-service access uses managed identities and traffic/data are protected with encryption in transit and at rest. We continuously monitor service health and security telemetry to detect and respond to issues quickly.

## How do you handle PII?

CheckID processes only the minimum identity attributes required to complete authentication and TAP creation, and does so transiently in-memory. We do not store, retain, or log personal data in CheckID.

The customer remains the Data Controller; identity records remain in the customer’s Entra ID.

## Who has access to CheckID Platform?

Access is restricted to authorized personnel only and is governed by Microsoft Entra, role-based access control, and privileged access workflows (PIM). Only approved administrators/operators can manage configuration, and access is controlled through auditable role assignments and least-privilege principles.

## If an issue occurs, how does Fortytwo notify customers?

If we detect an incident that may affect your service, we will proactively reach out to you directly. Our team monitors CheckID continuously, and when an issue is identified we notify affected customers through agreed channels; typically Microsoft Teams — rather than waiting for customers to report problems themselves. Critical incidents are acknowledged within one business day, and we will keep you updated as the situation develops until resolution.
