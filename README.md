# OxideLab

OxideLab is a GitLab rewrite using modern technology and a modern software architecture that is easier to use and deploy and is lighter on resources.
OxideLab should be especially beneficial for smaller scale deployments and smaller organizations where GitLab can be too complicated and resource intensive to deploy which forces people to use an alternative like Gitea.
OxideLab is written with a partitioned frontend and backend with a Svelte SPA on the frontend and a Rust API on the backend.
Only the GraphQL API is implemented, not the REST API, which may break certain tooling.
Both the frontend UI and the backend API exactly match GitLab so it should be a drop in replacement and existing tooling, libraries, and apps should work as long as they are using the GraphQL API.
Only the frontend and backend are rewritten, GitLab Runner (GitLab's CI implementation) is still used since it is written in Go.

Benefits over GitLab:

- much lighter on resources by switching from Rails to Rust
  - 4GB RAM minimum with GitLab -> TODO
  - 4 cores minimum with GitLab -> 1 core minimum for OxideLab
- better UX with less jankiness by switching from a combination of HAML, jQuery, and many Vue apps to one Svelte SPA
- easier to deploy TODO
- fetching from the API is faster by switching from Rails to Rust TODO

Benefits over Gitea:

- much more feature rich including GitLab CI
- integrates into and benefits from the pre-existing GitLab ecosystem

## Software stack

- Linux
- Nginx
- Svelte
- Rust
- PostgreSQL

## Development environment

## Deploying
