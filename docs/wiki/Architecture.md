# Chest X-ray CNN Research — Architecture

## System flow

```mermaid
flowchart TD
 A[Dataset source and license review] --> B[Patient-level train / validation / test split]
 B --> C[Image preprocessing]
 C --> D[CNN training]
 D --> E[Validation and tuning]
 E --> F[Held-out evaluation]
 F --> G[Document metrics and limitations]
 G --> H[Package verified model weights]
 H --> I[Build and validate inference API]
 I --> J[Connect static interface]
```

## Design notes

- Keep user-interface responsibilities separate from model, API and data-service responsibilities.
- Validate inputs at the application boundary and return clear error messages.
- Keep secrets and privileged credentials on the server side.
- Document the versions of data, dependencies and model artifacts used for reproducible results.
- Test the full user journey after deployment, not only the build step.

## Deployment boundary

GitHub Pages can host static HTML, CSS, JavaScript and prebuilt frontend assets. It cannot execute Python/Flask services, server-side React Router actions, private environment variables or database operations. Those parts require a separate backend or application host.
