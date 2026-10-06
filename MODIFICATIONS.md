# Compatibility modifications

## Repository

`gitnetbug/Real-ESRGAN`

## Files changed

| File | Original backup | Modification | Reason |
|---|---|---|---|
| `realesrgan/version.py` | N/A (file was missing/ignored upstream) | Added tracked package version metadata for Real-ESRGAN 0.3.0. | Prevents `ModuleNotFoundError` when importing Real-ESRGAN directly and allows pip metadata generation. |
| `setup.py` | `backups/original/setup.py` | Read the static `VERSION` file during metadata generation and remove obsolete `setup_requires` fetching. | Prevents modern pip metadata/build failures caused by legacy setuptools dependency fetching. |
| `.gitignore` | `backups/original/.gitignore` | Unignored `realesrgan/version.py`. | Ensures the required metadata file is included in the fork. |

All original source files modified in this change are preserved under `backups/original/`.
