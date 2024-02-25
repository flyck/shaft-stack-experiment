# SHAFT

The SHAFT stack allows you to create an app, defining only the database schema and the html forms. Creating an api layer and managing the frontend is completely dropped, while you still get a graphQL api for free, which can be embedded in third party tools for operations.

- [Backend]:
  - Sqlite db
  - [Tuql](https://github.com/bradleyboy/tuql) (sqlite schema -> graphql api)
  - Fly.io
    - [litefs](https://fly.io/docs/litefs/) for distributed sqlite
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

# Dev Notes

- Building something with HTMX for the first time is definitely a learning curve. There seem to be
  many ways to achieve a single thing. The docs are poetic and easy to read, but sometimes it
  seems that they lack more examples.
- The main goal of htmx doesnt seem to be to remove react. It is to avoid writing javascript at
  all cost, which happens to include react. Instead of writing javascript, html templates should
  be generated from the backend. Using HTMX with a nodejs typescript backend would be against the
  philosophy of htmx. Using a non-javacsript language like GO really does seem to be the intended
  use.
