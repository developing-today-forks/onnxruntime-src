# onnxruntime-src

Source mirror of [microsoft/onnxruntime](https://github.com/microsoft/onnxruntime) release trees,
submodules included, for reproducible Nix builds.

`github.com/microsoft/onnxruntime` has returned 404 since 2026-11-18
(developing-today/code#12247), so `fetchFromGitHub { tag = "v1.31.1"; fetchSubmodules = true; }`
can no longer fetch. Each release here carries `onnxruntime-<version>-src.tar.xz`, which unpacks to
the exact tree the upstream pin produced (same NAR hash):

| version | NAR hash (fetchzip) |
| ------- | ------------------- |
| 1.31.1  | `sha256-wATnI1v3De6+41fGYWS2458TCUWhBECNw2kBnfajKEo=` |

The source is MIT licensed by Microsoft; see `LICENSE` inside the tarball. This repo adds nothing
to it.
