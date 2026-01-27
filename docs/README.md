# TestLab API Documentation

This directory contains the complete API documentation for TestLab, built with [Mintlify](https://mintlify.com).

## Structure

```
docs/
├── mint.json                    # Mintlify configuration
├── introduction.mdx             # API overview and getting started
├── authentication.mdx           # Auth methods (API keys & Bearer tokens)
├── openapi.yaml                 # OpenAPI 3.0 specification
├── api-reference/              # API endpoint documentation
│   ├── test-cases/
│   ├── test-suites/
│   ├── executions/
│   ├── automated-results/
│   ├── api-keys/
│   ├── data/
│   └── reports/
└── guides/                      # Integration guides
    ├── quickstart.mdx
    ├── ci-cd-integration.mdx
    └── examples.mdx
```

## Local Development

To run the documentation locally:

```bash
# Install Mintlify CLI globally
npm install -g mintlify

# Or use it from package.json
npm run docs:dev
```

The documentation will be available at `http://localhost:3000`.

## Deployment

The documentation can be deployed to Mintlify's hosting platform or any static hosting service.

### Deploy to Mintlify

1. Sign up at [Mintlify](https://mintlify.com)
2. Connect your repository
3. Configure the docs directory path
4. Deploy!

### Build for Static Hosting

```bash
npm run docs:build
```

This will generate static files that can be hosted on Vercel, Netlify, or any other static hosting platform.

## Configuration

### Base URL

Update the `api.baseUrl` in `mint.json` to match your deployment:

```json
{
  "api": {
    "baseUrl": "https://testlab.letsmake.com"
  }
}
```

### Branding

Update colors, logo, and favicon in `mint.json`:

```json
{
  "colors": {
    "primary": "#3b82f6",
    "light": "#60a5fa",
    "dark": "#2563eb"
  },
  "logo": {
    "dark": "/logo/dark.svg",
    "light": "/logo/light.svg"
  }
}
```

## OpenAPI Specification

The `openapi.yaml` file contains the complete API specification. It's referenced by all API endpoint pages for consistency.

To validate the OpenAPI spec:

```bash
npx @redocly/cli lint openapi.yaml
```

## Writing Documentation

### Adding New Endpoints

1. Add the endpoint to `openapi.yaml`
2. Create an MDX file in the appropriate `api-reference/` subdirectory
3. Add the page to `mint.json` navigation

### Using Mintlify Components

Mintlify provides special components for documentation:

```mdx
<Card title="Example" icon="rocket" href="/path">
  Card content
</Card>

<Accordion title="FAQ Item">
  Answer content
</Accordion>

<Warning>
  Important warning message
</Warning>

<Info>
  Helpful information
</Info>
```

See the [Mintlify documentation](https://mintlify.com/docs) for more components.

## Support

For issues or questions about the documentation:
- Open an issue in the repository
- Contact support@letsmake.com
