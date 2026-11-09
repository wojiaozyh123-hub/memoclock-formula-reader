# Memo Clock formula reader

The handwriting-to-formula reader that the Memo Clock app downloads the first time it is used (about 183 MB). It turns a handwritten or photographed formula into LaTeX, on the device.

## Where it comes from

- Model: **TexTeller 1.0.2** by OleehyO — <https://github.com/OleehyO/TexTeller>, licensed under the Apache License 2.0. A copy of that license is in [LICENSE](LICENSE).
- Changes made here (no retraining): the encoder and decoder were converted to Core ML (the decoder keeps its key/value cache as Core ML state, so it needs iOS 18), their weights were quantized to 4 bits, and the tokenizer was written out as `tokens.json`.

## Files

The files are attached to the [releases](../../releases). A release asset cannot hold a folder, so every `/` in a file's path is written as `--` in its asset name, for example `Decoder.mlmodelc--weights--weight.bin` is `Decoder.mlmodelc/weights/weight.bin`. `manifest.json` lists every file with its path, size and SHA-256; the app checks each one before using it.
