---
license: apache-2.0
base_model: google/gemma-4-E2B-it
language: [ko, en]
tags: [gguf, llama.cpp, gemma4, korean, english, text-only]
---

# Wordborn models

Public, hash-pinned mirror of the on-device language model used by Wordborn, a
Korean/English story game. Release assets only; no user data, stories, or app source.

## Model

- File: `imat-IQ4XS-ple2-b43c251dac64.gguf` (content-addressed name of `imat-IQ4XS-ple2.gguf`)
- Size: 1,667,869,152 bytes
- SHA-256: `b43c251dac64541abff70cb0e9b2813255d8ac80307356f4ae95868386b58886`
- Release: https://github.com/neureps/wordborn-models/releases/tag/gemma4-e2b-enko-iq4xs-v1

The app downloads this file only after the user confirms, verifies the size and SHA-256,
and then runs it locally with llama.cpp. The model is not bundled with the app.

## Origin and modifications

- Base model: `google/gemma-4-E2B-it` at revision `3e22461f65e89153144f8adb70e3b8c2cc9845a7`,
  licensed under the Apache License 2.0 (https://ai.google.dev/gemma/docs/gemma_4_license).
- Modified by Neureps Inc.: vocabulary pruned to Korean and English (262,144 → 164,608 tokens),
  vision and audio components removed (text only), converted to GGUF, and quantized with a
  Korean/English importance matrix (IQ4_XS body, q2_K per-layer token embeddings, q4_K token
  embeddings). No additional training.
- This is not an official Google release, and no endorsement is implied.

See [LICENSE](LICENSE) (Apache License 2.0) and [NOTICE](NOTICE).
