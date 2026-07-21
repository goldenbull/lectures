# Welcome to [Slidev](https://github.com/slidevjs/slidev)!

To start the slide show:

- `pnpm install`
- `pnpm run dev`
- visit <http://localhost:3030>

Edit the [slides.md](./slides.md) to see the changes.

Learn more about Slidev at the [documentation](https://sli.dev/).

# deployment

`pnpm exec slidev build --base /quant-ai/ --without-notes`

caddy config:

```
        redir /quant-ai /quant-ai/
        handle_path /quant-ai/* {
                root * /var/www/lecture
                try_files {path} /index.html
                file_server
        }
```