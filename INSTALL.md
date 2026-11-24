# Installing Ariadne in Hermes Agent

> Ariadne is available under the [MIT License](LICENSE).

## Requirements

- A working Hermes Agent installation, configured with access to a model.
- The `ariadne/` directory from this package, including its four files in `references/`.
- Permission to read the philosophical materials you provide.

The steps below use a POSIX shell, as tested on macOS. Do not assume they are validated on Windows, Linux, or a different host. `HERMES_HOME` selects the target Hermes data directory; if unset, the commands use `~/.hermes`. Selecting an isolated data directory also isolates its configuration and may require separate provider authentication.

## Copy the Skill

In a terminal, change to the directory containing this `INSTALL.md` and the package’s `ariadne/` directory. Then run:

```sh
TARGET="${HERMES_HOME:-$HOME/.hermes}/skills/ariadne"
if [ -e "$TARGET" ] || [ -L "$TARGET" ]; then
  printf '%s\n' "A Skill already exists at $TARGET; stop and review it before installing."
else
  mkdir -p "$(dirname "$TARGET")"
  cp -R ./ariadne "$TARGET"
fi
```

The guard avoids intentionally replacing an existing installation. Do not continue if a same-named Skill is already present; decide how to preserve it first. If copying fails, inspect the error instead of assuming installation completed.

## Discover and use

Start a fresh Hermes session so the Skill index is refreshed. Check for `ariadne` with `hermes skills list`, then ask the assistant to load `ariadne` and supply your question or a text. If the Skill does not appear, check that `SKILL.md` is directly inside the target `ariadne/` folder and that the four references are in `ariadne/references/`. An active profile or `HERMES_HOME` may point at a different data directory.

If another philosophy-learning Skill is also available, its scope may overlap. Ask explicitly for Ariadne and inspect the session’s actual Skill-loading events when testing; naming the Skill does not itself prove which instructions the model followed.

## What was verified

On macOS with the local Hermes Agent checkout, a review copy was placed into a fresh, isolated data directory using `cp -R`. The Hermes CLI module’s `skills list` showed `ariadne` as enabled; the host’s `skill_view` implementation loaded the main file and each of the four references, with returned contents matching the installed files. This was a filesystem/install-and-load check, **not** an authenticated teaching session, a fresh-machine setup, or a verification of the `hermes` executable’s default interactive launch on another user’s system.

A model may need separate authentication; do not send credentials in a chat. Installation, Skill discovery and successful loading do not guarantee correct philosophical interpretation or that a model will choose a reference at the right time.
