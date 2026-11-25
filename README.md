# Poopy-McClauderson

Poopy-McClauderson is a humorous custom spinner configuration for Claude Code. It replaces Claude's standard spinner verbs with an extensive collection of toilet-, fart-, and other bathroom-themed phrases.

The configuration is stored in [`poopy.json`](poopy.json) using Claude Code's `spinnerVerbs` settings format:

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": [
      "Pinching a loaf",
      "Reading the shampoo bottle"
    ]
  }
}
```

## Install

Claude Code reads custom settings from a `settings.json` file.

1. Download or clone this repository:

   ```bash
   git clone https://github.com/seanrobertwright/Poopy-McClauderson.git
   cd Poopy-McClauderson
   ```

2. Open your Claude settings file:

   - **macOS or Linux:** `~/.claude/settings.json`
   - **Windows:** `%USERPROFILE%\.claude\settings.json`

   If the file or `.claude` directory does not exist, create them first.

3. Open [`poopy.json`](poopy.json) and copy its `spinnerVerbs` object:

   ```json
   "spinnerVerbs": {
     "mode": "replace",
     "verbs": [
       "..."
     ]
   }
   ```

4. Add `spinnerVerbs` to `settings.json`. If the file is empty, make it a valid JSON object like this:

   ```json
   {
     "spinnerVerbs": {
       "mode": "replace",
       "verbs": [
         "Pinching a loaf",
         "Reading the shampoo bottle"
       ]
     }
   }
   ```

   If `settings.json` already contains settings, merge the `spinnerVerbs` property into the existing top-level JSON object rather than creating a second object:

   ```json
   {
     "theme": "dark",
     "spinnerVerbs": {
       "mode": "replace",
       "verbs": [
         "Pinching a loaf",
         "Reading the shampoo bottle"
       ]
     }
   }
   ```

   With all of the repository's phrases, replace the example `verbs` array with the contents of `poopy.json`.

5. Save `settings.json`, then restart Claude Code to apply the new spinner verbs.

## Configuration behavior

- `mode: "replace"` replaces Claude Code's default spinner phrases with the phrases in `verbs`.
- The phrases are selected randomly while Claude is working.

## License

This project is licensed under the [MIT License](LICENSE).
