![saplings](https://github.com/kanopi/saplings/assets/5177009/a6377e32-deb2-49d8-873a-f3dd5a36fa7c)

# Saplings - AI Image Alt Text

Installs and configures image alt text generation tools.

## Features
- Generation of alt text using an AI provider.
- Adds to all image fields.
- Incorporates a human-in-the-loop review before saving.
- Uses the entity’s language to generate alt text in the appropriate language.
- Includes a bulk tool for generating al text for images that have none.

## Installation

```
composer require kanopi/saplings-ai-image-alt-text
cd web && php core/scripts/drupal recipe ../recipes/saplings-ai-image-alt-text
```

### Configure OpenAI

While the AI module supports many AI services, this recipe is configure to use
OpenAI.

1. Create an API key at https://platform.openai.com
2. Create a key file at `private://keys/openai_provider.key`. That is usually at
   `[webroot]/sites/default/files/private/keys/openai_provider.key`.
3. Once you are ready to deploy, be sure to place that key in your cloud
environments on the site's host. If you place it in the canonical environment,
it will get cloned on subsequent multidev clones.

## Usage

To use the configured AI tools, start by clicking the *Generate with AI* button
on any image form.

There is also a bulk edit tool that compiles a list of fields missing alt text
and fixes them in bulk. This tool is located at Admin > Configuration > Media.
