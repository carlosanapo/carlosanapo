# Preview the site locally

Docker is the simplest option because it includes the Ruby and Jekyll versions the site needs.

## Docker (recommended)

From the repository root, run:

```bash
docker compose pull
docker compose up
```

Open <http://localhost:8080>. Changes to the site content should appear automatically after a few seconds. Press `Ctrl+C` to stop the server.

To run it in the background instead:

```bash
docker compose up -d
docker compose logs -f
```

Stop the background server with:

```bash
docker compose down
```

## Native Ruby

If Ruby, Bundler, Node.js, and ImageMagick are already installed:

```bash
bundle install
npm ci
npm run lint:prettier
npm run lint:style-contract
bundle exec jekyll build
bundle exec jekyll serve
```

Open <http://localhost:4000>. Stop the server with `Ctrl+C`.

The public GitHub Pages address is configured as <https://carlosanapo.github.io>, so `baseurl` must remain empty.
