# Self-media Title Rewriter

A free Chinese title-rewriting Skill with no third-party API key required. It keeps the facts in your brief, produces three differentiated titles each for Douyin, Xiaohongshu, and Bilibili, and recommends the title that best matches the body. It does not promise virality or expand into video production or publishing.

## Use it now

Provide a core benefit, body text, and one or more platforms. The Skill returns copy-ready titles plus a concise recommendation. If a required field is absent, it identifies the missing material instead of inventing facts. See [the successful fixture](fixtures/success-output.md).

## Scope

- Built for Chinese independent creators and small-shop operators.
- Uses only supplied, verifiable facts; optional audience, tone, and restricted words are welcome.
- Produces titles and a recommendation reason only.
- No browser, account, or external service is required, so it never accesses login state or publishing platforms.

## Validate

```bash
node scripts/self-test.mjs
node ../skill-seo/scripts/audit.mjs --root . --output /tmp/selfmedia-title-lab-cn-seo --strict
```

The workflow, copy, and code are original. Public projects consulted only for business use and licensing context are listed in the Chinese README.
