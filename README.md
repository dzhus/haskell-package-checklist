# Haskell package maintenance checklist

## General considerations

### `package.yaml`

- [ ] CHANGELOG.md and README.md are in extra-source-files
- [ ] -Wall and -Wcompat are enabled
- [ ] Tests
- [ ] Benchmarks
- [ ] Doctests

### `README.md`

- [ ] Travis badge
- [ ] Hackage badge
- [ ] packdeps badge
- [ ] Code examples in README (possibly markdown-unlit example)

### `.travis.yml`

- [ ] Travis builds tests, haddocks and benchmarks, uses --pedantic

### GitHub repo

- [ ] Branch protection enabled for master
- [ ] Hackage link in GitHub project URL
- [ ] Hackage synopsis matches GitHub description

## Making a release

- [ ] README and CHANGELOG look ok on GitHub
- [ ] The latest CHANGELOG entry matches the new version
- [ ] stack sdist
- [ ] stack upload
- [ ] Tag the head and push to master
