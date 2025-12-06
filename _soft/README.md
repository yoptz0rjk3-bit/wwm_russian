# Tools / Утилиты

[Русский](#русский) | [English](#english)

## Русский
### Обзор
Вспомогательные скрипты и GUI для работы с переводами.

### multitool
- `tsv_transfer_gui.py` — GUI для TSV: перенос новых ID A→B, замена строк по ID, удаление дублей, проверки (формат/теги/китайские/сломанные параметры), поиск/вырезка/замена по тексту, debug TSV с UUID-тегами.
- `sort_master.py` — GUI сортировки TSV по правилам `sort.txt`; строит порядок по исходному файлу и применяет к целевому; может фильтровать только совпавшие строки.

### transfer
- `old_to_new.py` — перенос ключей/значений между версиями переводов/словарями (ID, OriginalText).

### packing_unpacking
- `WWM_Extractor_Files_and_Texts_2.py`, `WWM_Extractor_Files_and_Texts.py` — распаковка/запаковка файлов игры, извлечение/сборка текста (CSV/TSV), полная цепочка data+text.
- `README.md` — детали по упаковке/распаковке.

### other
- `match_dictionary.py` — сопоставление словарей/ID между файлами.
- `count_mentions.py` — подсчёт вхождений слов/ID.

## English
### Overview
Helper scripts and GUIs for translation workflows.

### multitool
- `tsv_transfer_gui.py` — TSV GUI: transfer new IDs A→B, replace rows by ID, deduplicate, validators (format/tags/Chinese/broken params), text search/cut/replace, debug TSV with UUID tags.
- `sort_master.py` — TSV sort GUI using `sort.txt` rules; builds ordering from a source file and applies it to a target; can filter only matched rows.

### transfer
- `old_to_new.py` — move keys/values between translation versions/dictionaries (ID, OriginalText).

### packing_unpacking
- `WWM_Extractor_Files_and_Texts_2.py`, `WWM_Extractor_Files_and_Texts.py` — game file unpack/pack, text extract/pack (CSV/TSV), full data+text pipeline.
- `README.md` — details for packing/unpacking.

### other
- `match_dictionary.py` — match dictionaries/IDs across files.
- `count_mentions.py` — count occurrences of words/IDs.

