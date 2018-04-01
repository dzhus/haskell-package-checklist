# Haskell package maintenance checklist

## General considerations

### `package.yaml`

- [ ] [CHANGELOG.md][] and README.md are in extra-source-files
- [ ] -Wall and [-Wcompat][] are enabled
- [ ] [Doctests][]
- [ ] Tests (with [doctest-discover][])
- [ ] Benchmarks

### `README.md`

- [ ] Travis badge
- [ ] Hackage badge
- [ ] packdeps badge
- [ ] Code examples in README (possibly [markdown-unlit][] example)

### `.travis.yml`

- [ ] Travis builds tests, haddocks and benchmarks, uses --pedantic

### GitHub repo

- [ ] Branch protection enabled for master
- [ ] Hackage link in GitHub project URL
- [ ] Hackage synopsis matches GitHub description

## Making a release

- [ ] README and CHANGELOG look ok on GitHub
- [ ] stack sdist
- [ ] The latest CHANGELOG entry matches the new version
- [ ] stack upload
- [ ] Tag the head and push to master

[-wcompat]: https://downloads.haskell.org/~ghc/8.4.1/docs/html/users_guide/using-warnings.html#ghc-flag--Wcompat

[changelog.md]: https://keepachangelog.com/en/1.0.0/

[doctests]: https://github.com/sol/doctest

[doctest-discover]: https://github.com/karun012/doctest-discover

[markdown-unlit]: https://github.com/sol/markdown-unlit
