# Toolchain builder (GitHub Releases)

Этот репозиторий автоматически собирает Android‑native toolchain и публикует его в GitHub Releases.

## Что внутри toolchain

Берём upstream:
- `bnsmb/clang19_toolchain_for_android`

Workflow делает:
- клонирует upstream tag
- запускает `sysroot/create_tar_archive.sh`
- переименовывает архив в предсказуемое имя
- считает `sha256`
- публикует Release assets

## Как запустить

GitHub → Actions → **Build toolchain release** → Run workflow:\n
- `tag`: `v1`\n
- `upstream_tag`: `v1.5.0_21.09.2025`\n

## Выходные файлы

- `androidcppide-toolchain-arm64-v8a-v1.tar.gz`\n
- `androidcppide-toolchain-arm64-v8a-v1.tar.gz.sha256`\n

