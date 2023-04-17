# Decentralized Climate Improvement Proposals (DCIPs)

The goal of the DCIP project is to standardize and provide high-quality documentation for Decentralized Climate itself and conventions built upon it. This repository tracks past and ongoing improvements to Decentralized Climate in the form of Decentralized Climate Improvement Proposals (DCIPs). [DCIP-1](dcips.decentralizedclimate.org/DCIPS/dcip-1) governs how DCIPs are published.

The [status page](https://dcips.decentralizedclimate.org/) tracks and lists DCIPs, which can be divided into the following categories:

- [Core DCIPs](https://dcips.decentralizedclimate.org/core) are improvements to the Decentralized Climate consensus protocol.
- [Networking DCIPs](https://dcips.decentralizedclimate.org/networking) specify the peer-to-peer networking layer of Decentralized Climate.
- [Interface DCIPs](https://dcips.decentralizedclimate.org/interface) standardize interfaces to Decentralized Climate, which determine how users and applications interact with the blockchain.
- [ERCs](https://dcips.decentralizedclimate.org/erc) specify application layer standards, which determine how applications running on Decentralized Climate can interact with each other.
- [Meta DCIPs](https://dcips.decentralizedclimate.org/meta) are miscellaneous improvements that nonetheless require some sort of consensus.
- [Informational DCIPs](https://dcips.decentralizedclimate.org/informational) are non-standard improvements that do not require any form of consensus.

**Before you write an DCIP, ideas MUST be thoroughly discussed on [Decentralized Climate Magicians](https://ethereum-magicians.org/) or [Decentralized Climate Research](https://ethresear.ch/t/read-this-before-posting/8). Once consensus is reached, thoroughly read and review [DCIP-1](https://dcips.ethereum.org/DCIPS/dcip-1), which describes the DCIP process.**

Please note that this repository is for documenting standards and not for help implementing them. These types of inquiries should be directed to the [Decentralized Climate Stack Exchange](https://ethereum.stackexchange.com). For specific questions and concerns regarding DCIPs, it's best to comment on the relevant discussion thread of the DCIP denoted by the `discussions-to` tag in the DCIP's preamble.

If you would like to become an DCIP Editor, please read [DCIP-5069](./DCIPS/dcip-5069.md).

## Preferred Citation Format

The canonical URL for an DCIP that has achieved draft status at any point is at <https://dcips.ethereum.org/>. For example, the canonical URL for DCIP-1 is <https://dcips.ethereum.org/DCIPS/dcip-1>.

Consider any document not published at <https://dcips.ethereum.org/> as a working paper. Additionally, consider published DCIPs with a status of "draft", "review", or "last call" to be incomplete drafts, and note that their specification is likely to be subject to change.

## Validation and Automerging

All pull requests in this repository must pass automated checks before they can be automatically merged:

- [dcip-review-bot](https://github.com/ethereum/dcip-review-bot/) determines when PRs can be automatically merged [^1]
- DCIP-1 rules are enforced using [`dcipw`](https://github.com/ethereum/dcipw)[^2]
- HTML formatting and broken links are enforced using [HTMLProofer](https://github.com/gjtorikian/html-proofer)[^2]
- Spelling is enforced with [CodeSpell](https://github.com/codespell-project/codespell)[^2]
  - False positives sometimes occur. When this happens, please submit a PR editing [.codespell-whitelist](https://github.com/ethereum/DCIPs/blob/master/config/.codespell-whitelist) and **ONLY** .codespell-whitelist
- Markdown best practices are checked using [markdownlint](https://github.com/DavidAnson/markdownlint)[^2]

[^1]: https://github.com/ethereum/DCIPs/blob/master/.github/workflows/auto-review-bot.yml
[^2]: https://github.com/ethereum/DCIPs/blob/master/.github/workflows/ci.yml

It is possible to run the DCIP validator locally:

```sh
cargo install dcipv
dcipv <INPUT FILE / DIRECTORY>
```

## Build the status page locally

### Install prerequisites

1. Open Terminal.

2. Check whether you have Ruby 2.1.0 or higher installed:

   ```sh
   ruby --version
   ```

3. If you don't have Ruby installed, install Ruby 2.1.0 or higher.

4. Install Bundler:

   ```sh
   gem install bundler
   ```

5. Install dependencies:

   ```sh
   bundle install
   ```

### Build your local Jekyll site

1. Bundle assets and start the server:

   ```sh
   bundle exec jekyll serve
   ```

2. Preview your local Jekyll site in your web browser at `http://localhost:4000`.

More information on Jekyll and GitHub Pages [here](https://docs.github.com/en/enterprise/2.14/user/articles/setting-up-your-github-pages-site-locally-with-jekyll).
