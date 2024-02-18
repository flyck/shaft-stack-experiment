# SHAFT

- [Backend]:
  - Sqlite db
  - [Tuql](https://github.com/bradleyboy/tuql) (sqlite schema -> graphql api)
  - Fly.io
    - ([litefs](https://fly.io/docs/litefs/) for distributed sqlite
    - containers app to host the tuql nodejs express api
    - fly can also host static pages
- [Frontend]:
  - Htmx
  - Astro

<p align="center">
  <img src=".assets/logo_dalle.png" alt="Your Logo" width="150" height="auto">
</p>


## Maybe

- [ ] Try Clerk for easy auth

## Fly.io Free Tier

Resources included for free on all plans ([docs](https://fly.io/docs/about/pricing/#free-allowances)):
- Up to 3 shared-cpu-1x 256mb VMs
- 3GB persistent volume storage (total)
- 160GB outbound data transfer
