# Reversible Computation (RC) website

This repository contains the source of the <https://reversible-computation.github.io/> website.

- In `_config.yml` is the base information of the site.
- In `_data/meny.yml` the menu item can be edited as a yml-list.

## Local testing

You can deploy [the website locally](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll) to test it.
In short:

- [Install Jekyll](https://jekyllrb.com/docs/installation/),
- Clone this repository, enter it,
- Run

    ```console
    gem install bundler jekyll
    bundle install
    bundle exec jekyll serve
    ```
- Navigate to <http://127.0.0.1:4000/>, or whichever URL is given in the terminal output.
    
If you want a fresh start, try

```console
bundle clean --force
```

and re-execute the commands above.

    
## Policy

Please, be aware that the following policy is enforced:

https://github.com/reversible-computation/reversible-computation.github.io/blob/1d5d0eb11b5f974c82ffaa932f531ccfd4baaff6/_layouts/default.html#L38

As a consequence, inline style & scripts are not possible.

## Testing

You can make sure the website gets good scores at

- <https://www.accessibilitychecker.org/audit/?website=https%3A%2F%2Freversible-computation.github.io> (Accessibility)
- <https://pagespeed.web.dev/analysis/https-reversible-computation-github-io/2xdxrtberi?form_factor=mobile> (General)
- <https://securityheaders.com/?q=https%3A%2F%2Freversible-computation.github.io%2F> (Security headers -- disclaimer: we don't)

for example.

## Various notes

- Except for the index.md page at root level, all pages uses the topmost title `h1` as the title page. The index.md page at top level uses a separate `title:` field in its yaml header to list its name as simply "Home", and the template prepends `Reversible Computation (RC) -` to all page titles.
- Redirection or aliasing is supported thanks to [JekyllRedirectFrom](https://github.com/jekyll/jekyll-redirect-from): simply add

    ```yml
    redirect_from:
    - /old-url/
    ```
    
    in the `/new-url/index.md` ["front matter"](https://jekyllrb.com/docs/front-matter/) to redirect `/old-url/` to `/new-url/`. This plug-in is added and whitelisted in `_config.yml`.
