# Shared shelf setups

`avni-shelves.json` is one person's shelf setup:

- **AI research:** seven topic sub-shelves (Pre-training, Post-training, Architecture & infra, Evals, Interpretability, Harness, Other), with paper sites like arXiv and OpenReview filed there.
- **Work:** three sub-shelves, with no site rules.
- **Social:** an empty top-level shelf.
- **Auto-sort:** on for AI research and Everything else, so Claude files new tabs by topic.

It has no per-tab assignments or personal URLs.

## Try it

This needs the `nested-shelves` features, so build from this branch first. Auto-sort also needs [Claude Code](https://claude.com/claude-code) installed and signed in.

```bash
./build.sh "$HOME/Applications"
# Quit Reading Desk (⌘Q) before loading.
hooks/load-config config/avni-shelves.json --dry-run   # preview
hooks/load-config config/avni-shelves.json
open -a "$HOME/Applications/Reading Desk.app"
```

`load-config` replaces your shelves, pinned sites and auto-sort switches. It backs up your current settings first and prints the exact command to restore them. Tabs you moved by hand keep their placement if the shelf they're on still exists.
