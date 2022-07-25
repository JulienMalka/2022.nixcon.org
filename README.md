# Website for NixCon 2022

Copied from https://github.com/cko/nixcon2017

## Build

The site is built with [Hakyll](https://jaspervdj.be/hakyll/)

    ghc --make site.hs
    site build
    site server

Watch and recompile for changes with `site watch`

### Build with nix

    nix-build

## FIXME: Travis Deployment

```sh
ssh-keygen -f deploy-key
travis encrypt-file --org -r nixcon/2020.nixcon.org deploy-key
rm deploy-key
git add travis-deployment
# ...git commit & push
```

Then go to https://github.com/nixcon/2020.nixcon.org/settings/keys and add the
`deploy-key.pub` to the deploy keys, with write access.

## License

The content of the website is licensed under the [Creative Commons Attribution Share Alike 4.0 International](LICENSES/CC-BY-SA-4.0.txt) license.

The software (including sample code) is licensed under the [MIT](LICENSES/MIT.txt) license.

Some files might have a different license. See the files content for details.
