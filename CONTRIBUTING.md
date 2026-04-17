# Contributing to the Top.gg Docs

Thanks for helping improve the Top.gg documentation! This repo powers [docs.top.gg](https://docs.top.gg), and we welcome fixes, clarifications, new examples, and community library submissions.

This is a repo maintained by a small team with a light review process. If you're fixing a typo, just open a PR. For bigger changes, skim the guidelines below first.

## Repo Structure

- `/api` - REST API reference pages (v0 and v1)
- `/libraries` - Official and community SDK pages
- `/webhooks` - Webhook docs and event reference
- `/resources` - Rate limits, auth, and other educative blog-style topics
- `docs.json` - Navigation, theme, and site config

## Writing Style

Keep it simple and practical. A few conventions we follow:

- **Second person, active voice.** "You can fetch votes with…" not "Votes can be fetched by the user."
- **Show, don't just tell.** Endpoint pages should have a working example and an SDK snippet where it makes sense.
- **Prefer short sentences.** If a sentence has three commas, it probably wants to be two sentences.
- **Code samples go in ` ```language ` fences** with the language specified. For multi-language examples, use Mintlify's `<CodeGroup>` component.
- **Callouts sparingly.** `<Note>` for helpful context, `<Warning>` for footguns, `<Tip>` for shortcuts. If every page has five callouts, none of them mean anything.
- **Link to other docs pages with relative paths** (`/api/v1/votes`), and to external sites with full URLs.
- **v0 vs v1.** Make it clear which version a page applies to. If an endpoint exists in both, document them separately.

## Adding a New SDK Library

We list community-maintained libraries on the [Libraries](https://docs.top.gg/libraries/javascript) page. To submit yours:

1. Open a PR adding a new page under `/libraries/` following the structure of the existing language pages (`javascript.mdx`, `python.mdx`, etc.).
2. Include installation instructions, a minimal code example, and a link to the library's repo.
3. The library should be **actively maintained** and cover at least stats posting + vote fetching.
4. Add the new page to `docs.json` so it shows up in the sidebar.

We'll take a quick look and merge if it's in good shape. We may ask for tweaks if the examples don't match our house style.

## Commits & PRs

- **Branches.** Target `main`. Name your branch something descriptive (`fix/webhook-signature-example`, `docs/add-rust-sdk`).
- **Commits.** No strict format, just write clear messages. If you're making several unrelated changes, please split them into separate commits.
- **PR titles.** Short and descriptive. Prefix with the area if it helps: `[v1] Clarify cursor pagination on /votes`.
- **One logical change per PR.** A typo sweep across ten files is one PR. Adding a new SDK is another. Don't mix them.

We squash-merge, so don't worry about tidying up your commit history before submitting.

## Questions?

If you're unsure whether a change is worth submitting, open an issue or draft PR and ask. We'd rather have the conversation early than send you back to the drawing board after you've written a bunch.
