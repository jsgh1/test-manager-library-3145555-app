# Manager Library — Operator web application

React + Vite, with token authentication and role-aware screens for the 10 user stories.

## Start

Copy `.env.example` to `.env` and set the API base URL. Then run `npm install` and `npm run dev`. You can also start it with the sibling `infra` Compose configuration.

- Admin: catalogue creation/edit/soft deletion and covers, member creation, librarian registration, borrowing, per-item returns, overdue lines and historical report.
- Librarian: catalogue, members, loans, returns and overdues; no admin-only actions.
- The UI consumes `/api/v1` with bearer JWT. Use valid administrator credentials from your deployment environment.
- The public marketing website is in the separate `page` repository and does not contact the API.

### Known limitations
The loan form currently uses the paginated, independently loaded books/member directories and needs a manual acceptance walkthrough with populated data. A first pass of the web interface is not evidence that the full contract or responsive behavior has been verified.
