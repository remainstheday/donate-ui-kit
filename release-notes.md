# Release Notes

> NOTE: before running a release you will need to use `npm login`

To cut a new release, you can use the following command locally:

```bash
npm version minor -m "Release %s"
```

You can replace `minor` with the type of release you want:

```
major - x.0.0
minor - 1.x.0
patch - 1.1.x
```

The command will automatically run the following actions:

- `build` to create new `dist` files
- add and commit changes to git
- create a tag with the new version
- push changes up to origin
- run an `npm publish` to push to npm