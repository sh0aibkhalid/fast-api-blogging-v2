# Contributor guide — fast-api-blogging-v2

A FastAPI blogging service: JWT auth, SQLAlchemy models, router/repository split under `blog/`.

## Working agreement

- One focused change per branch. Do not bundle unrelated fixes.
- Match the existing layout: routes in `blog/routers/`, data access in `blog/repository/`,
  Pydantic models in `blog/schemas.py`, ORM models in `blog/models.py`.
- Never commit `.env`, `blog.db`, or any real credential. `.env.example` holds placeholders only.
- Raise `HTTPException` with the correct status code — 401 for authentication, 403 for
  authorisation, 404 only for genuinely missing resources.

## Commits

- Conventional Commits: `type(scope): imperative summary`, subject under 72 characters.
- Body explains *why*, in two or three sentences. No bullet dumps of the diff.
- Never use placeholder words — no "test", "temp", "qa", "hello", "foo", "wip", "asdf" — in
  commit messages, branch names, code, sample data or fixtures. Sample data uses realistic
  names, emails and prose.

## Pull requests

- Title matches the commit subject.
- Body has three sections: **Context** (the problem), **Change** (what you did),
  **Verification** (how you confirmed it works).
