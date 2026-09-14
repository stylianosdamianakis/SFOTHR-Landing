# SFOTH: Reforged

Landing page for [sfothr.com](https://sfothr.com) — Sword Fights on the Heights IV: Reforged.

The page is a static GitHub Pages site with three links: the [Roblox game](https://www.roblox.com/games/77483797026305/Sword-Fights-on-the-Heights-IV-Reforged), the [wiki](https://wiki.sfothr.com/), and [Discord](https://discord.gg/sfoth).

## Preview locally

From this folder:

```powershell
python -m http.server 8080
```

Then open http://localhost:8080.

## Deploy

Pushes to `main` publish through [GitHub Actions](.github/workflows/pages.yml). The custom domain is `sfothr.com`.

## DNS

Keep the `wiki` CNAME pointing at Miraheze so [wiki.sfothr.com](https://wiki.sfothr.com) stays up. Apex and `www` should point at GitHub Pages:

| Type | Host | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |
| CNAME | `www` | `stylianosdamianakis.github.io` |
