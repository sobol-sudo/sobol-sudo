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
- [**keda** #7932](https://github.com/kedacore/keda/pull/7932) — merged. `AwsSecretManagerHandler.Initialize`
  dereferenced optional credentials without a nil check, so a `TriggerAuthentication` the CRD accepts as
  valid took the operator down. A maintainer ran the AWS Secret Manager e2e suite against real
  infrastructure before merging.

Currently open:

- [**TanStack Query** #11128](https://github.com/TanStack/query/pull/11128) — a thenable kept for
  React's optimistic unwrapping could end up reporting `rejected` while the promise had fulfilled,
  because a retained `reject` bypassed the guard that clears it. Adds the missing unit suite too.
- [**nitro** #4488](https://github.com/nitrojs/nitro/pull/4488) and
  [#4491](https://github.com/nitrojs/nitro/pull/4491) — two prerender routes can resolve to one output
  file, which Nuxt generates on its own for SPA builds. The writes were neither atomic nor deduplicated,
  so the file could ship torn between two renders — the write itself tore in 172 of 200 runs in isolation.
- [**vueuse** #5554](https://github.com/vueuse/vueuse/pull/5554) — `useRouteParams` and `useRouteQuery`
  share a per-router write queue, and a disposed scope left its pending write behind for an unrelated
  navigation to apply.
- [**react-spectrum** #10366](https://github.com/adobe/react-spectrum/pull/10366) — approved, awaiting a
  second reviewer. Three types appear structurally in the public `ButtonProps` but aren't re-exported from
  `react-aria-components`, so a project emitting declarations around `Button` fails with TS2883.

### Contact

[Telegram](https://t.me/sobolpe) · sobol4156@gmail.com
