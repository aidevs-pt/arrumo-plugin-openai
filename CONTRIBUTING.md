# Contributing

Thank you for helping improve the OpenAI plugin for Arrumo AI Video Editor. Bug reports, fixes, translations, documentation and
ideas are all welcome. You can write in English, Spanish or Portuguese.

## Before you start

- **Found a security problem?** Don't open an issue. Follow [SECURITY.md](SECURITY.md).
- **Questions and ideas** go to [Discussions](https://github.com/aidevs-pt/arrumo-video-editor/discussions). **Bugs** go to this repository's
  issues, one per problem.
- **For anything larger than a small fix,** open an issue first so we can agree on the approach
  before you spend time on it.
- Everyone taking part follows our [Code of Conduct](CODE_OF_CONDUCT.md).

## Develop

Before opening a pull request, package the plugin with the SDK, adding `--include` for every
adapter or tool file the manifest uses:

```sh
python3 ../../plugin-sdk/tools/package_plugin.py . /tmp/plugin.zip --include <file>
```

Install the ZIP in Arrumo (**Settings › Plugins › Import ZIP**) and try the change with a real
workspace. CI checks the manifest, icon and translations on
every push. The [Plugin SDK reference](https://www.aidevs.pt/tools/arrumo/docs/developer/sdk) documents every manifest field and
adapter schema.

## Guidelines

- **Keep provider-specific behaviour in this plugin**, through the Plugin SDK contracts.
- **Plugin text is translated** in the manifest's `translations` for English, Spanish and
  Portuguese.
- **Small, focused commits** with [Conventional Commits](https://www.conventionalcommits.org/)
  messages, such as `fix(render): keep the last frame when a clip ends early`.
- **Tests for behaviour changes.** Bug fixes include a test that fails without the fix.
- **Never commit API keys, account data, footage, exports or machine-specific settings.** Keys live
  in the creator's system vault.

## Pull requests

1. Fork the repository and create a branch from `main`.
2. Make your change, with tests and documentation.
3. Open a pull request and fill in the template. CI must pass.
4. The first time you contribute, a bot asks you to sign the
   [Contributor License Agreement](CLA.md) by replying with a comment. You sign it once per
   repository.
5. A maintainer reviews the change. We squash-merge, so the pull request title becomes the commit
   message.

## Labels

Maintainers label issues and pull requests so you can find work and see where things stand:

- **Kind:** `bug`, `enhancement`, `documentation`, `refactor`, `tests`, `ci`, `security`,
  `performance`, and `breaking change` for changes to a public contract. `dependencies` marks
  automated dependency updates.
- **Platform:** `platform: windows`, `platform: macos` or `platform: linux` when only one system is
  affected.
- **Status:** `status: stacked` builds on another open pull request, so merge that one first;
  `status: blocked` waits on something outside it; `status: needs maintainer` needs an action only
  a maintainer can take.
- **Getting started:** `good first issue` and `help wanted` mark work that is ready to pick up.

You don't need to label your own pull request. If you think a label applies, say so in the
description.

## License

This project is licensed under the [GNU Affero General Public License v3.0](LICENSE) and owned by DEVS.AI UNIPESSOAL LDA. The [CLA](CLA.md) lets DEVS AI distribute your contribution under this
license and under other terms in the future; you keep the copyright to your work.
