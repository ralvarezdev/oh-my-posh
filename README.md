# oh-my-posh

My [Oh My Posh](https://ohmyposh.dev) prompt configuration.

## Files

- **`ralvarezdev.omp.json`** — My customised theme (config `version` 4). Segments carry `_comment` fields naming the terminal colour tokens used (for example `term-purple`, `term-blue`).
- **`jandedobbeleer.omp.json`** — A near-identical variant that also enables git status and upstream icon fetching and adds a `battery` segment to the right prompt. The name suggests it is based on the `jandedobbeleer` theme that ships with Oh My Posh.

## Prompt layout

- **Left** — `session` (user name), `path` (folder style, `~` home icon), `git` (branch truncated to 25 characters), `node`, `go`, `python`, `executiontime` (always shown) and `status`.
- **Right** (`ralvarezdev.omp.json`) — `shell`, `sysinfo` (physical memory usage) and `time`.

The console title template is `{{ .Shell }} in {{ .Folder }}` and `final_space` is enabled. In `ralvarezdev.omp.json`, git `fetch_status` and `fetch_upstream_icon` are off. Segments use Nerd Font icons, so set a Nerd Font in your terminal.

## Usage

Install Oh My Posh, then initialise your shell with one of the configs.

```sh
eval "$(oh-my-posh init bash --config /path/to/oh-my-posh/ralvarezdev.omp.json)"
```

```powershell
oh-my-posh init pwsh --config "C:\path\to\oh-my-posh\ralvarezdev.omp.json" | Invoke-Expression
```
