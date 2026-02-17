# logos

A lightweight CDN service for serving SVG logos via API. Hosted at [logos.agentictrust.com](https://logos.agentictrust.com).

## API

### Get a logo

```
GET /api/{slug}
```

Returns the SVG file for the given slug. Case-insensitive.

**Example:** `https://logos.agentictrust.com/api/slack` returns the Slack logo as `image/svg+xml`.

Response headers include strong caching (`max-age=432000, immutable`) and ETag support.

### List all logos

```
GET /api/list
```

Returns a JSON map of all available logo slugs to their URLs.

## Local development

```bash
bun install
bun dev
```

Open [http://localhost:3000/api/list](http://localhost:3000/api/list) to see all available logos.

## Stack

- [Next.js](https://nextjs.org) 15 (Pages Router)
- TypeScript
- 1,248 SVG logos in `src/assets/`

## License

MIT
