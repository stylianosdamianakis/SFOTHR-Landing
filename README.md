# SFOTH: Reforged landing page

Static one-page site for [sfothr.com](https://sfothr.com), published with GitHub Pages.

Decorate `index.html` and `styles.css`. Put images in `assets/`. The Discord, wiki, and Roblox links are already wired.

## One-time GitHub Pages setup

After the first push to `main`, GitHub Actions publishes the site. Then:

1. Open [Pages settings](https://github.com/stylianosdamianakis/SFOTHR-Landing/settings/pages).
2. Confirm the source is **GitHub Actions**.
3. Set **Custom domain** to `sfothr.com` and save.
4. Wait for DNS to check out, then enable **Enforce HTTPS**.

Until the custom domain is live, the site is at:

https://stylianosdamianakis.github.io/SFOTHR-Landing/

## DNS for sfothr.com

The domain currently shows a Squarespace "coming soon" page. In your DNS settings, replace the apex and `www` Squarespace records with GitHub Pages.

Leave the existing `wiki` CNAME (it should point at `sfothr.miraheze.org`) so [wiki.sfothr.com](https://wiki.sfothr.com) keeps working.

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

Remove any old A / CNAME / forwarding records on `@` and `www` that still point at parking or a different host. DNS and HTTPS can take up to an hour after you save.

## Preview locally

Open `index.html` in a browser, or from this folder:

```powershell
python -m http.server 8080
```

Then visit http://localhost:8080.
