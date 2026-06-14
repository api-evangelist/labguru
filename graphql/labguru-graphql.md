# Labguru GraphQL API

## Description

Labguru is an electronic laboratory notebook (ELN) and biotech data management platform for life sciences organizations including biotech, pharma, CRO, food tech, and academic institutions. The platform provides unified API access for managing experiments, protocols, samples, inventory, equipment, and research project data.

Labguru's API documentation references GraphQL support alongside its REST API. The GraphQL interface is intended to provide flexible, query-driven access to lab data entities including experiments, protocols, inventory items, samples, reagents, equipment, storage locations, notebooks, projects, users, and collaboration permissions.

## Endpoint

- **GraphQL Endpoint**: `https://app.labguru.com/graphql`
- **Developer Docs**: https://www.labguru.com/developer-tools
- **API Introduction**: https://help.labguru.com/en/articles/6149483-api-introduction-and-overview

## Authentication

Labguru APIs use token-based authentication. The authentication token must be passed with each request. See https://help.labguru.com/en/articles/2946290-r-api-authentication for details.

## Notes on GraphQL Support

- Labguru's primary public API documentation focuses on REST endpoints (v1 and v2).
- The GraphQL endpoint at `https://app.labguru.com/graphql` is referenced in platform documentation but requires an authenticated session tied to a specific lab account subdomain (e.g., `https://<account>.labguru.com/graphql`).
- Introspection may be disabled or gated behind authentication on the public endpoint.
- The schema in `labguru-schema.graphql` is a conceptual SDL schema derived from Labguru's documented REST data model, covering the core life science lab management entities.

## Core Data Domains

- **Research**: Experiments, Protocols, Notebooks, ExperimentSections, Attachments
- **Project Management**: Projects, Milestones, Tasks, Workflows
- **Inventory**: Samples, Reagents, Materials, StockItems, Storage, Locations
- **Equipment**: Equipment, Instruments
- **Collaboration**: Users, Teams, CollaborationPermissions
- **Procurement**: Orders, Invoices

## References

- REST API Changelog: https://help.labguru.com/en/articles/9571977-api-docs-change-log
- Python SDK: https://github.com/BioData/LabguruPython
- R SDK: https://github.com/BioData/LabguruR
- API Examples: https://github.com/BioData/labguru-api-examples
