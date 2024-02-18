# SHAFT

- [Backend]:
  - Sqlite db
  - Tuql (sqlite schema -> graphql api)
  - Fly.io
    - ([litefs](https://fly.io/docs/litefs/) for distributed sqlite
    - containers app to host the tuql nodejs express api
    - fly can also host static pages
- [Frontend]:
  - Htmx
  - Astro

## Maybe

- [ ] Try Clerk for easy auth

## Fly.io Free Tier

Resources included for free on all plans ([docs](https://fly.io/docs/about/pricing/#free-allowances)):
- Up to 3 shared-cpu-1x 256mb VMs
- 3GB persistent volume storage (total)
- 160GB outbound data transfer
