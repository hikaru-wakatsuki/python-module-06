*This project has been created as part of the 42 curriculum by hwakatsu.*

# The Codex

## Description / 説明

### English
The Codex is a Python project focused on understanding the import system through a small alchemy-themed package. Its goal is to learn how Python packages are structured, how `__init__.py` controls package exposure, how different import styles work, how absolute and relative imports differ, and how circular dependencies can be avoided.

The repository is organized around four practical parts:

- `ft_sacred_scroll.py`: demonstrates package initialization and package-level exposure through `alchemy/__init__.py`
- `ft_import_transmutation.py`: demonstrates multiple import styles such as full-module imports, specific imports, aliases, and multiple imports
- `ft_pathway_debate.py`: demonstrates absolute imports in `alchemy/transmutation/basic.py` and relative imports in `alchemy/transmutation/advanced.py`
- `ft_circular_curse.py`: demonstrates validation and late imports to avoid circular dependencies in `alchemy/grimoire`

Based on the code in this repository, the project includes:

- an `alchemy` package exposing only selected elemental functions at package level
- simple element and potion functions that return strings
- a transmutation subpackage that combines absolute and relative import techniques
- a grimoire subpackage that uses a late import inside `record_spell()` to avoid circular import problems

### 日本語
The Codex は、小さな錬金術テーマのパッケージを通して Python の import システムを理解するためのプロジェクトです。目的は、Python パッケージの構造、`__init__.py` による公開制御、複数の import スタイル、絶対 import と相対 import の違い、そして循環依存の回避方法を学ぶことです。

このリポジトリは、4 つの実践パートで構成されています。

- `ft_sacred_scroll.py`: `alchemy/__init__.py` によるパッケージ初期化と公開制御を実演
- `ft_import_transmutation.py`: モジュール全体 import、特定関数 import、別名 import、複数 import を実演
- `ft_pathway_debate.py`: `alchemy/transmutation/basic.py` の絶対 import と `alchemy/transmutation/advanced.py` の相対 import を実演
- `ft_circular_curse.py`: `alchemy/grimoire` におけるバリデーションと late import による循環依存回避を実演

このリポジトリのコードでは、次の内容が含まれています。

- パッケージレベルでは一部の要素関数だけを公開する `alchemy` パッケージ
- 文字列を返すシンプルな element 関数と potion 関数
- 絶対 import と相対 import の両方を使う transmutation サブパッケージ
- `record_spell()` の中で late import を使い、循環 import 問題を回避する grimoire サブパッケージ

## Instructions / 実行方法

### English

Requirements:

- Python 3.10 or later
- No external dependencies

Run the demonstration scripts from the repository root:

```bash
python3 ft_sacred_scroll.py
python3 ft_import_transmutation.py
python3 ft_pathway_debate.py
python3 ft_circular_curse.py
```

Optional lint check:

```bash
flake8 .
```

There is no installation or compilation step. The project relies only on the Python standard library and local package files.

### 日本語

必要環境:

- Python 3.10 以上
- 外部依存関係なし

リポジトリのルートで、各デモスクリプトを次のように実行できます。

```bash
python3 ft_sacred_scroll.py
python3 ft_import_transmutation.py
python3 ft_pathway_debate.py
python3 ft_circular_curse.py
```

任意の lint チェック:

```bash
flake8 .
```

インストールやコンパイルは不要です。このプロジェクトは Python 標準ライブラリとローカルパッケージのみを使用します。

## Features / 主な内容

### English

- `alchemy/__init__.py` exposes `create_fire` and `create_water` while keeping other element functions package-hidden.
- `alchemy/potions.py` combines imported element functions to build potion result strings.
- `alchemy/transmutation/basic.py` uses absolute imports from `alchemy.elements`.
- `alchemy/transmutation/advanced.py` uses relative imports from sibling and parent modules.
- `alchemy/grimoire/spellbook.py` imports the validator inside the function to avoid a circular dependency at import time.

### 日本語

- `alchemy/__init__.py` は `create_fire` と `create_water` を公開し、それ以外の element 関数はパッケージレベルでは隠しています。
- `alchemy/potions.py` は import した要素関数を組み合わせて potion の結果文字列を生成します。
- `alchemy/transmutation/basic.py` は `alchemy.elements` からの絶対 import を使います。
- `alchemy/transmutation/advanced.py` は兄弟モジュールや親パッケージからの相対 import を使います。
- `alchemy/grimoire/spellbook.py` は import 時の循環依存を避けるため、関数内で validator を import しています。

## Project Structure / 構成

### English

- [`alchemy/__init__.py`](/Users/hikaru/project/42/python6/alchemy/__init__.py): package interface and metadata
- [`alchemy/elements.py`](/Users/hikaru/project/42/python6/alchemy/elements.py): basic element functions
- [`alchemy/potions.py`](/Users/hikaru/project/42/python6/alchemy/potions.py): potion functions built from imported elements
- [`alchemy/transmutation`](/Users/hikaru/project/42/python6/alchemy/transmutation): absolute vs relative import examples
- [`alchemy/grimoire`](/Users/hikaru/project/42/python6/alchemy/grimoire): validation and late import example
- [`ft_sacred_scroll.py`](/Users/hikaru/project/42/python6/ft_sacred_scroll.py): package exposure demo
- [`ft_import_transmutation.py`](/Users/hikaru/project/42/python6/ft_import_transmutation.py): import-style demo
- [`ft_pathway_debate.py`](/Users/hikaru/project/42/python6/ft_pathway_debate.py): pathway comparison demo
- [`ft_circular_curse.py`](/Users/hikaru/project/42/python6/ft_circular_curse.py): circular dependency avoidance demo

### 日本語

- [`alchemy/__init__.py`](/Users/hikaru/project/42/python6/alchemy/__init__.py): パッケージ公開インターフェースとメタデータ
- [`alchemy/elements.py`](/Users/hikaru/project/42/python6/alchemy/elements.py): 基本 element 関数
- [`alchemy/potions.py`](/Users/hikaru/project/42/python6/alchemy/potions.py): import した element を組み合わせる potion 関数
- [`alchemy/transmutation`](/Users/hikaru/project/42/python6/alchemy/transmutation): 絶対 import と相対 import の例
- [`alchemy/grimoire`](/Users/hikaru/project/42/python6/alchemy/grimoire): バリデーションと late import の例
- [`ft_sacred_scroll.py`](/Users/hikaru/project/42/python6/ft_sacred_scroll.py): パッケージ公開デモ
- [`ft_import_transmutation.py`](/Users/hikaru/project/42/python6/ft_import_transmutation.py): import スタイルのデモ
- [`ft_pathway_debate.py`](/Users/hikaru/project/42/python6/ft_pathway_debate.py): import 経路比較デモ
- [`ft_circular_curse.py`](/Users/hikaru/project/42/python6/ft_circular_curse.py): 循環依存回避デモ

## Resources / 参考資料

### English

Classic references related to the topic:

- [Python Documentation: The import system](https://docs.python.org/3/reference/import.html)
- [Python Documentation: Modules](https://docs.python.org/3/tutorial/modules.html)
- [Python Documentation: Packages](https://docs.python.org/3/tutorial/modules.html#packages)
- [PEP 328: Imports](https://peps.python.org/pep-0328/)
- [Real Python: Python Imports 101](https://realpython.com/python-import/)
- [flake8 Documentation](https://flake8.pycqa.org/)

AI usage in this project:

- AI was used for documentation support and README writing.
- It was used to review the repository structure, summarize how each import example works, and produce bilingual English/Japanese explanations.
- The README was aligned with the existing code under `alchemy/` and the four `ft_*.py` scripts, while the implementation itself should still be reviewed manually and understood for evaluation.

### 日本語

この課題に関連する代表的な参考資料:

- [Python Documentation: The import system](https://docs.python.org/3/reference/import.html)
- [Python Documentation: Modules](https://docs.python.org/3/tutorial/modules.html)
- [Python Documentation: Packages](https://docs.python.org/3/tutorial/modules.html#packages)
- [PEP 328: Imports](https://peps.python.org/pep-0328/)
- [Real Python: Python Imports 101](https://realpython.com/python-import/)
- [flake8 Documentation](https://flake8.pycqa.org/)

このプロジェクトにおける AI の利用:

- AI はドキュメント補助に使用しました。

## Notes / 補足

### English
The project keeps all formulas intentionally simple and returns strings so that the focus remains on package structure and import behavior rather than algorithmic complexity.

### 日本語
このプロジェクトでは、アルゴリズムの複雑さではなくパッケージ構造と import の挙動に集中できるよう、すべての関数を意図的にシンプルにし、文字列を返す設計にしています。
