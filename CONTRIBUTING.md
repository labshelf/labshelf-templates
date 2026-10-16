# Contributing a template

LabShelf's Publish template command opens the pull request for you. To submit by hand:

1. Fork this repository and add `templates/<id>/`. The id uses lowercase letters and digits joined by single hyphens, and equals the folder name.
2. Add `template.yaml`, the project files under `files/`, and `preview/thumbnail.png` and `preview/sample.pdf`. Compile the sample yourself with the engine named in the manifest, without shell-escape.
3. Run `node validate.mjs` and fix every message it prints.
4. Open a pull request. CI runs the same validator.

`index.json` is generated. Do not edit it: CI rebuilds it after every merge that changes `templates/`.

The rules every template must meet are in [README.md](README.md#review-rules).
