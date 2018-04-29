# Haskell package maintenance checklist

## General considerations

### `package.yaml`

- [ ] [CHANGELOG.md][] and README.md are in extra-source-files
- [ ] -Wall and [-Wcompat][] are enabled
- [ ] [Doctests][]
- [ ] Tests (with [doctest-driver-gen][])
- [ ] Benchmarks

### `README.md`

- [ ] Travis badge

      [![Travis CI build status](https://travis-ci.org/user-name/repo-name.svg)](https://travis-ci.org/user-name/repo-name)

- [ ] Hackage [badge][shields]

      [![Hackage](https://img.shields.io/hackage/v/package-name.svg?colorB=5e5184&style=flat)](https://hackage.haskell.org/package/package-name)

- [ ] packdeps [badge][shields]

      [![Hackage deps](https://img.shields.io/hackage-deps/v/package-name.svg)](http://packdeps.haskellers.com/feed?needle=package-name)

- [ ] Code examples in README (possibly [markdown-unlit][] example)

### `.travis.yml`

- [ ] [hlint][]
- [ ] Travis builds tests, haddocks and benchmarks, uses `--pedantic`

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

[doctests]: https://github.com/sol/doctest#readme

[doctest-driver-gen]: https://github.com/Hexirp/doctest-driver-gen#readme

[markdown-unlit]: https://github.com/sol/markdown-unlit#readme

[hlint]: https://github.com/ndmitchell/hlint#running-with-continuous-integration

[shields]: https://shields.io/
