# Tools / Утилиты

RU: Краткое описание вспомогательных скриптов и GUI для работы с переводами.

EN:  A brief description of auxiliary scripts and GUIs for working with translations.

## multitool

- `tsv_transfer_gui.py` — GUI для TSV: перенос новых ID A→B, замена строк по ID, удаление дублей, проверки (формат, теги, китайские символы, сломанные параметры), поиск/вырезка по тексту, создание debug TSV с UUID.GUI for TSV: transfer new IDs A→B, replace rows by ID, dedup, validators (format, tags, Chinese chars, broken params), text search/cut, debug TSV with UUID tags.
- `sort_master.py` — GUI сортировки TSV по словам из `sort.txt` с учётом дубликатов: строит порядок из исходного файла и применяет к целевому; умеет фильтровать только совпавшие строки.
  TSV sort GUI using `sort.txt` word rules; builds ordering from source file, applies to target; can filter matches only.

## transfer

- `old_to_new.py` — перенос данных между версиями переводов/словари (переезд ключей/значений).
  Move data between translation versions/dictionaries (keys/values migration).

## packing_unpacking

- `WWM_Extractor_Files_and_Texts_2.py`, `WWM_Extractor_Files_and_Texts.py` — распаковка/запаковка файлов игры, извлечение/сборка текста (CSV/TSV), полная цепочка data+text.Game file unpack/pack, text extract/pack (CSV/TSV), full data+text pipeline.
- `README.md` — детали по упаковке/распаковке.
  Details for packing/unpacking.

## other

- `match_dictionary.py` — сопоставление словарей/ID между файлами.Dictionary/ID matching across files.
- `count_mentions.py` — подсчёт вхождений слов/ID.
  Count occurrences of words/IDs.
