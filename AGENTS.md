# Repository guidance

## 1. What this project is

This repository is a self-contained training lab about project instructions for Codex (`README.md`). Its learner starter is a small checkout example: `calculate_total(items)` calculates a cart total and returns a float (`learner/starter/README.md`, `learner/starter/src/checkout.py`). Lab instructions and templates are in `learner/`; the starter project is in `learner/starter/` (`README.md`).

## 2. Technology and structure

- Use Python and the standard library for the starter. The documented tests use `unittest`, and the README says no package installation is required (`learner/starter/README.md`, `learner/starter/tests/test_checkout.py`).
- Follow the existing small structure: implementation in `src/checkout.py`, tests in `tests/test_checkout.py` (`learner/starter/README.md`). Do not introduce additional frameworks, dependencies, or architecture unless the task requires them.
- The public function is `calculate_total(items)`. Each item uses `price` and `quantity`; the current implementation returns a float (`learner/starter/src/checkout.py`).

## 3. Conventions

- Read the relevant task card, implementation, and tests before changing the starter (`learner/starter/task_card.md`, `learner/starter/src/checkout.py`, `learner/starter/tests/test_checkout.py`).
- Preserve existing calls and the float return contract unless the task explicitly changes them (`learner/starter/src/checkout.py`, `learner/starter/task_card.md`).
- Keep formatting separate from calculation when working on Task B (`learner/starter/task_card.md`).
- Keep changes within the requested task. For Task A, do not add dependencies or change the item schema (`learner/starter/task_card.md`).
- If requirements are ambiguous or conflict with the observed contract, state the uncertainty and ask for clarification before making a consequential choice.

## 4. Testing changes

The visible starter tests cover a single line item, multiple items, an empty cart, and the float return type (`learner/starter/tests/test_checkout.py`). Keep relevant coverage and add focused tests for each behavior changed. Use the task card's acceptance cases when implementing its tasks (`learner/starter/task_card.md`):

- **Task A (discount):** retain a call that passes only `items`; test 0%, 10%, and 100% discounts; test values below 0 and above 100 raise `ValueError`; verify the result remains a float. The task requires the range 0–100 inclusive (`learner/starter/task_card.md`).
- **Task B (formatting):** test `format_total` with a whole-dollar value and a fractional value; verify the output has a `$` prefix and exactly two digits after the decimal point. Keep the calculation function unchanged unless tests reveal a bug (`learner/starter/task_card.md`).

Run the complete documented test suite from `learner/starter/` after making changes:

```sh
python3 -m unittest discover -s tests -v
```

The starter README documents this command and says no package installation is required (`learner/starter/README.md`). Report whether it was run and its actual result, including failures; never claim a check passed if it was not run. If you cannot run it, state that clearly and give the reason.

## 5. Avoid

- Do not change application code or tests unrelated to the requested task.
- Do not add dependencies or change the item schema for Task A (`learner/starter/task_card.md`).
- Do not combine display formatting with the calculation when working on Task B (`learner/starter/task_card.md`).
- Do not invent project requirements when details are missing; identify the uncertainty and seek clarification when it affects the implementation.

## 6. Completion report

After completing a task, summarize the changes and name the files changed. State the verification command and actual result, or say clearly if it was not run. Mention any unresolved ambiguity or limitation. These reporting instructions are workflow guidance for this lab.
