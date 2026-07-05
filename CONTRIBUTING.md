# Contributing

This is an open project. Fork it, change it, build your own — and if you make it better, send it back.

## Ways to contribute

- **Share your build.** Built one of these (or your own variant)? Post it — photos, parts swaps, what you'd do differently. The best community builds get featured. → [Share your build](https://github.com/autonomous-ai/autonomous-computer/issues/new?template=share-your-build.md)
- **Improve a guide.** Fix a wrong step, a dead link, a better assembly order, clearer wording. PRs welcome.
- **Suggest better parts.** Found a cheaper PSU, a quieter fan, a better board? Open an issue or PR with the swap and why.
- **Fill in the software.** [`setup.md`](setup.md) covers BIOS, drivers, and hardware verification — real, tested improvements from your own build are the highest-value contribution right now.
- **Ask a question.** Stuck on a build? → [Ask a build question](https://github.com/autonomous-ai/autonomous-computer/issues/new?template=build-question.md)

## How to submit a change

1. Fork the repo and create a branch.
2. Make your change. Keep the structure: each build is self-contained in its folder at the repo root (`2x/`, `4x/`, `8x/` — its own `bom/`, `docs/`, `photos/`, `step_models/`, `stl-models/`); the shared software doc is `setup.md`.
3. Check your links and image paths resolve (GitHub is case-sensitive).
4. Open a pull request describing what you changed and why.

## Repo layout

```
2x/         Home build
4x/         Team build
8x/         On-prem business build
setup.md    BIOS, drivers, testing (shared)
```

## License

By contributing, you agree your contributions are licensed under the repo's [MIT License](LICENSE).
