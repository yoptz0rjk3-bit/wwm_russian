# Multitool — README

[English](#english) | [Русский](#русский)

## English
### Overview
GUI utilities for TSV workflows: ID sync/cleanup/validation (`tsv_transfer_gui.py`) and word-based sorting with duplicate grouping (`sort_master.py`).

### Files
- `tsv_transfer_gui.py` — TSV maintenance GUI: transfer new IDs A→B, replace rows by ID, deduplicate, validators (format/tags/Chinese/broken params), text search/cut/replace, debug TSV with UUID tags.
- `sort_master.py` — TSV sort GUI using `sort.txt` rules; builds ordering from a source file and applies it to a target file; can filter only matching rows.

### Requirements
- Install once from repo root: `pip install -r ../requirements.txt` (PyQt5, pyzstd).

### tsv_transfer_gui.py — main actions
- Transfer: copy new IDs from A to B.
- Replace by ID: overwrite matching rows in B with rows from A.
- Remove duplicates: keep rows with Cyrillic text first, drop others.
- Validators: format check, tag check, find Chinese characters, find broken `ru_ru` params.
- Text ops (on B): find IDs by text, delete by text, replace rows from A by text match, cut matching rows to `select_*.tsv`.
- Debug: add `[UUID]` tags to `OriginalText` and maintain `{name}_uuid.tsv`.
- External validators are expected in `.github/scripts` relative to repo root.

### sort_master.py — sorting and filtering
- Uses `sort.txt` (one rule per line): `word:text` allows `word` + `s/'s`; `word:own` matches whole word only.
- Two directions: “Sort from” builds priority mask on source; “Sort to” applies that order to target by ID.
- Modes:
  - Full sort: reorder entire target using source ranking (score + text, then ID).
  - Filter: keep only rows whose IDs matched word rules in source, ordered by source ranking.
- Output is written as `*_sort.tsv` next to the target file; originals are not modified.

### Tips
- Place `sort.txt` alongside your TSV; the app auto-detects it but you can pick manually.
- Columns should include `ID` and `OriginalText`; defaults fall back to first/second column if absent.

## Русский
### Обзор
GUI-утилиты для TSV: синхронизация/чистка/проверка ID (`tsv_transfer_gui.py`) и сортировка по словам с учётом дублей (`sort_master.py`).

### Файлы
- `tsv_transfer_gui.py` — GUI для TSV: перенос новых ID A→B, замена строк по ID, удаление дублей, проверки (формат/теги/китайские/сломанные параметры), поиск/вырезка/замена по тексту, debug TSV с UUID-тегами.
- `sort_master.py` — GUI сортировки TSV по правилам `sort.txt`; строит порядок по исходному файлу и применяет к целевому; может фильтровать только совпавшие строки.

### Требования
- Однократно установить: `pip install -r ../requirements.txt` (PyQt5, pyzstd).

### tsv_transfer_gui.py — основные действия
- Перенос: копировать новые ID из A в B.
- Замена по ID: перезаписать строки в B данными из A.
- Удаление дублей: оставить строку с кириллицей, остальные удалить.
- Проверки: формат TSV, теги, китайские символы, сломанные `ru_ru` параметры.
- Операции по тексту (для B): найти ID, удалить, заменить строками из A, вырезать в `select_*.tsv`.
- Debug: добавить `[UUID]` в `OriginalText`, вести `{name}_uuid.tsv`.
- Внешние валидаторы ищутся в `.github/scripts` относительно корня репо.

### sort_master.py — сортировка и фильтрация
- `sort.txt` (по строке на правило): `word:text` допускает `word` + `s/'s`; `word:own` — строго целое слово.
- Направления: «Сортировать из» строит приоритет на исходнике; «Сортировать в» применяет порядок к целевому по ID.
- Режимы:
  - Полная сортировка: упорядочить весь целевой по рангу исходника (score + текст, потом ID).
  - Вырезать: оставить только строки, чьи ID совпали по словам в исходнике, в порядке исходника.
- Результат сохраняется как `*_sort.tsv` рядом с целевым; исходники не меняются.

### Подсказки
- Кладите `sort.txt` рядом с TSV; можно выбрать вручную.
- Нужны колонки `ID` и `OriginalText`; при отсутствии берутся первая/вторая.

