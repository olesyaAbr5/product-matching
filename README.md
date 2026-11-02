# Product matching

Поиск одинаковых товаров маркетплейса: классификация пар товаров «один и тот же товар / разные» по названиям и атрибутам.

- `Data_analysis.ipynb` - разведочный анализ товаров и размеченных пар
- `Levenshtein.ipynb` - расстояние Левенштейна между названиями как признак
- `Pairs_preparation.ipynb` - сборка таблицы пар с названиями и атрибутами обоих товаров
- `Attributes.ipynb` - разбор JSON-атрибутов (бренд, артикул, партномер), поиск кандидатов бренда в названиях и создание признака пары `brand_common`
- `Features.ipynb` - признаки похожести названий (fuzz, Жаккар) и их ROC-AUC
- `Numbers.ipynb` - исследование числовых полей, разница массы и Жаккар по числам из названий
- `Feature_assembly.ipynb` - проверка и сборка общей таблицы признаков
- `data/raw/` - исходные данные: `items_human.parquet`, `matches.parquet`, `matches_llm.parquet`
- `data/` - подготовленные пары, извлечённые характеристики и признаки; parquet-файлы в репозиторий не входят

## Где сохраняются результаты

- `Features.ipynb` → `data/name_features.parquet`: fuzz и Жаккар по словам.
- `Attributes.ipynb` → `data/pairs_attrs.parquet`, `data/brand_candidates.parquet`, `data/brand_features.parquet`.
- `Numbers.ipynb` → `data/weight_features.parquet` и `data/number_features.parquet`.
- `Feature_assembly.ipynb` → `data/features.parquet`: общая таблица.



