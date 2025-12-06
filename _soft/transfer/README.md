# Transfer — README

[English](#english) | [Русский](#русский)

## English
### Overview
Utility scripts for moving data between translation versions/dictionaries.

### Files
- `old_to_new.py` — migrates keys/values from an old translation file to a new one (TSV/CSV with `ID`, `OriginalText`); helps align updated bases without losing existing translations.

### Requirements
- Install once from repo root: `pip install -r ../requirements.txt` (PyQt5, pyzstd) — only standard library is typically used here.

### Usage (generic outline)
- Prepare old and new translation files (TSV/CSV).
- Run the script to map IDs and carry over texts where IDs match; inspect output for missing or new IDs.
- Keep originals intact; work on copies until verified.

## Русский
### Обзор
Скрипты для переноса данных между версиями переводов/словарями.

### Файлы
- `old_to_new.py` — переносит ключи/значения из старого файла перевода в новый (TSV/CSV с `ID`, `OriginalText`); помогает выровнять обновлённые базы без потери переведённых строк.

### Требования
- Однократно установить: `pip install -r ../requirements.txt` (PyQt5, pyzstd) — здесь обычно хватает стандартной библиотеки.

### Использование (общее)
- Подготовьте старый и новый файлы перевода (TSV/CSV).
- Запустите скрипт, чтобы перенести тексты по совпадающим ID; проверьте отчёт по пропущенным/новым ID.
- Оригиналы не трогайте: работайте с копиями до проверки результата.

