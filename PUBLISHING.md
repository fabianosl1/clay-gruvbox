# Publishing Modern Gruvbox

## Prepare the public repository

The manifest currently targets `https://github.com/fabianosl1/modern-gruvbox`. Create that public repository, or update the `repository` field in `extension.toml` to the actual URL before submitting.

Push the local `main` branch to the public repository. No GitHub repository or Zed registry submission is created by this local package.

Before submitting:

- Test the extension through `zed: install dev extension` in Zed.
- Check highlighting in your usual languages and inspect diagnostics, search, selections, and terminal colors.
- Add a real Zed screenshot to the README for the release presentation.
- Keep `extension.toml` version `0.1.0` consistent with the registry entry.

## Submit to the Zed registry

Follow the [official publishing guide](https://zed.dev/docs/extensions/publishing/publishing-guide), [prerequisites](https://zed.dev/docs/extensions/publishing/prerequisites), and [license requirements](https://zed.dev/docs/extensions/publishing/license-requirements).

1. Fork and clone `zed-industries/extensions`.
2. Create a submission branch in your fork.
3. Add the public theme repository as a submodule:

   ```sh
   git submodule add https://github.com/fabianosl1/modern-gruvbox extensions/modern-gruvbox
   ```

4. Add this entry to the registry's `extensions.toml`:

   ```toml
   [modern-gruvbox]
   submodule = "extensions/modern-gruvbox"
   version = "0.1.0"
   ```

5. Run `pnpm sort-extensions`, commit, push your submission branch, and open a pull request to `zed-industries/extensions`.

The submodule URL must use HTTPS. The submitted commit must be available on a branch in the public repository. Publication follows review and merge by Zed maintainers.

## Updates

Increment the version in `extension.toml`, commit and push the theme changes, then update the submodule commit and matching version in the Zed extensions registry through a new pull request.
