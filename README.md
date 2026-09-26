# `.github`

Organization-level files for [Ghoti.io](https://github.com/Ghoti-io). No
code, and nothing any library depends on.

GitHub gives this repository name a fixed meaning: a few paths inside it are
read as defaults for the whole organization rather than as ordinary files.
That is the entire reason it exists, and it is why the name cannot be
anything else.

| Path | What GitHub does with it |
| --- | --- |
| `profile/README.md` | Rendered on <https://github.com/Ghoti-io> as the organization's landing page |

Anything else GitHub reads from here — issue and pull-request templates,
workflow templates, a `FUNDING.yml`, a default `CODE_OF_CONDUCT.md` — would
be a default that any repository in the organization can override with its
own copy. Nothing of that kind is here yet; when something is added, add its
row above, because the paths are conventions rather than anything this
repository can declare.

**Start at [`suite`](https://github.com/Ghoti-io/suite)** if you are looking
for the libraries — how to clone them, build them, and read the manual.
