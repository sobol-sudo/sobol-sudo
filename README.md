## Alexander Kolesnik

Senior Fullstack Engineer, 6 years in production. I lead frontend work on [AI/ML API](https://aimlapi.com)
at Boiler Labs — a platform that serves 1000+ AI models behind a single OpenAI-compatible endpoint.

Frontend is where I'm deepest — Vue 3 / Nuxt 3 and TypeScript — but I own features end to end: the
NestJS service, the Postgres migration and the CI pipeline are mine when that's what shipping takes.
Most of my work is the unglamorous half of a product people actually pay for: SSR that doesn't flicker,
checkout flows that survive real payment providers, and pages that stay fast when the API doesn't
cooperate.

**Stack** — TypeScript · Vue 3 / Nuxt 3 · React / Next.js · NestJS · PostgreSQL · ClickHouse · Docker · GitHub Actions

### Open source

- [**recharts** #7582](https://github.com/recharts/recharts/pull/7582) — merged. Bars ignored the
  requested `barGap` whenever `maxBarSize` clamped the computed width. Open for 4.5 years; fixed with
  unit tests and a visual-regression case.
- [**fastify** #6872](https://github.com/fastify/fastify/pull/6872) — merged. The `requestIdHeader`
  docs stated two contradictory defaults; traced the conflict to a v4-into-v5 merge and corrected it.
- [**openlayers**](https://github.com/openlayers/openlayers/pull/17576) — two merged. `offsetX` was
  silently dropped for text placed along a line (open 20 months), and
  [WFS 2.0.0 transactions](https://github.com/openlayers/openlayers/pull/17583) wrote a filter element
  that only exists in WFS 1.x, which GeoServer rejects.
- [**storybook** #35589](https://github.com/storybookjs/storybook/pull/35589) — merged. The `next/link`
  mock ignored `trailingSlash`, so Storybook rendered hrefs the running app never would. A maintainer
  spotted that the Vite plugin ships its own copy of the same mock, so I closed that half too in
  [vite-plugin-storybook-nextjs #136](https://github.com/storybookjs/vite-plugin-storybook-nextjs/pull/136).

### Contact

[Telegram](https://t.me/sobolpe) · sobol4156@gmail.com
