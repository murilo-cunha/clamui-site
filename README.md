# clamui

**AI edits you review before they land.**

clamui is a markdown editor with Claude built in. Every suggestion arrives as a
side-by-side diff — you **Accept** or **Reject**. Nothing touches your file until
you say so.

This isn't a preference, it's enforced at the tool level: the Edit and Write tools
that would let Claude write directly to disk are disabled. Every change arrives
through the reviewed-diff pipeline, or it doesn't arrive at all.

🌐 **[Landing page](https://murilo-cunha.github.io/clamui-site/)** · 📦 **[Releases](https://github.com/murilo-cunha/clamui-site/releases)**

## Features

- **WYSIWYG markdown** — headings, bold, lists, blockquotes, and images render
  inline as you type, while the file on disk stays byte-exact markdown.
- **Your own Claude subscription** — sign in with your existing Claude account via
  OAuth. No API key.
- **Reviewed diffs, enforced** — Claude's direct-write tools are disabled; every
  edit shows up as a green/red side-by-side diff you accept or reject.
- **Review at keyboard speed** — accept with <kbd>⌘⏎</kbd>, reject with
  <kbd>⌘⌫</kbd>, hop between staged edits with <kbd>Tab</kbd>, and <kbd>⌘Z</kbd>
  re-stages the last decision.
- **⌘K inline edits** — select text and prompt Claude in place, with
  <kbd>@</kbd>-mentions that autocomplete your project's files and follow-ups that
  refine a staged diff.
- **New files are reviewed too** — a brand-new file arrives as a create-diff;
  nothing exists on disk until you accept it.
- **Bring your MCP connectors** — clamui discovers the MCP servers you've already
  set up for Claude Code and adds them to the session with a click.
- **Tools ask before they act** — in ask mode, every external tool call surfaces
  as an allow/deny prompt.
- **Export via pandoc** — render the document to docx, HTML, or PDF, locally.
- **Dark, light, or system theme** — switches instantly and persists.
- **Esc means stop** — a generation going the wrong way stops immediately, not
  after the turn finishes.
- **Updates arrive in-app** — install once, get new versions from the update
  prompt on launch.

## Install

### macOS (Apple silicon)

With Homebrew:

```sh
brew tap murilo-cunha/clamui
brew install clamui
```

Or download **[clamui_aarch64.dmg](https://github.com/murilo-cunha/clamui-site/releases/latest/download/clamui_aarch64.dmg)**
and drag clamui to Applications. The binary is unsigned, so the first launch needs
right-click → **Open**. Updates arrive in-app after that.

### VS Code extension

Download **[clamui.vsix](https://github.com/murilo-cunha/clamui-site/releases/latest/download/clamui.vsix)**
(the link always serves the newest release) and install it:

```sh
code --install-extension clamui.vsix
```

Then open any `.md` file → right-click its tab → *Reopen Editor With…* →
**clamui Markdown**.

---

This repo hosts the landing page and public releases for clamui; the source repo
is private.
