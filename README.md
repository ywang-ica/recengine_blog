# RecEngine Tech Blog

This repository hosts the RecEngine team's technical blog, built with the
[Chirpy][chirpy] Jekyll theme and prepared for GitHub Pages deployment.

## What Is Here

- A team-branded Jekyll blog for technical writing
- GitHub Pages workflow under `.github/workflows/pages-deploy.yml`
- Starter content for the landing page, About page, and first post

## Local Development

The easiest local path is to use the devcontainer.

### Devcontainer

1. Open the repo in VS Code.
2. Run `Dev Containers: Reopen in Container`.
3. Wait for the post-create step to finish `bundle install`.
4. Start the blog:

```bash
bash tools/run.sh
```

5. Open:

```text
http://localhost:4000/
```

6. Run a local build and content check:

```bash
bash tools/test.sh
```

7. Stop the local server:

```text
Press Ctrl+C in the terminal running `bash tools/run.sh`
```

## Deployment Assumption

The current `_config.yml` is set up as a GitHub Pages project site for:

`https://ywang-ica.github.io/recengine-blog`

For local development, `tools/run.sh` also loads `_config_dev.yml`, which sets
`baseurl: ""` so the landing page is available directly at:

`http://localhost:4000/`

If you later move the blog to a custom domain or a different GitHub owner, update
`url` and `baseurl` in `_config.yml`.

## License

The site uses the [MIT][mit]-licensed Chirpy starter and theme ecosystem.

[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE
