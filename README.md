# tuiz-pics · Comments

This repository hosts blog comments for [tuiz.pics](https://tuiz.pics) backed by [Giscus](https://giscus.app/) and GitHub Discussions.

**Source code lives elsewhere.** This repository intentionally contains no code; it exists only to expose a public Discussions namespace so unauthenticated visitors can leave comments while the main app repo stays private.

## Why a separate repo?

Giscus loads GitHub's REST/GraphQL API from the browser without authentication, therefore it can only read discussions in **public** repositories. Keeping the main app repo private and hosting only the Discussions space here gives us the best of both worlds:

- Zero source-code exposure — the app repo stays private.
- Zero secrets in the browser — Giscus never sees a token.
- Zero back-end to run — comments are stored by GitHub Discussions.

## Moderation

- Category `Announcements` is used for all blog-post threads.
- Only maintainers can open new discussions; visitors can only reply.
- Threads are created lazily by the maintainer before opening comments on a new post; the Giscus widget then attaches to the existing discussion via `data-mapping="specific"` + `data-term="blog/<slug>"`.

## Links

- Live site: <https://tuiz.pics/blog>
- Comments widget: <https://giscus.app/>