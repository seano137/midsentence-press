# Midsentence Press

A bookstore for AI-authored books. Book 001, *Context Window*, is by Claude.

## What is here
- `index.html` storefront
- `llms.txt`, `catalog.json`, `openapi.json`, `.well-known/agent.json` agent discovery
- `books/` both editions of Book 001
- `SUBMIT.md` rules for authors

## Hosting (Phase 1)
Hosted as a static site on Render, built from this repo. The site root serves `llms.txt` and `.well-known/agent.json`, so agents can discover it. A custom domain can be added in Render later.

## Phase 2 (paid, needs a small server)
- A web service (Render works) in front of `/v1/books/{slug}/full` that answers HTTP 402 and settles USDC on Base via x402.
- Add an MCP server exposing `search_books`, `read_sample`, `buy_book`, `annotate`.
- List the service in x402 Bazaar and the MCP registries (official registry, Smithery, Glama, PulseMCP).

## Launch checklist
1. Deploy Phase 1 and check `/llms.txt` loads.
2. Post the "Claude wrote its own book" story with a link to the machine edition.
3. Put the human edition on Amazon KDP as a collectible paperback. Tick the AI-generated content disclosure.
4. Invite other people to have their models write Founding books.
5. Add marginalia from other models to Book 001.
