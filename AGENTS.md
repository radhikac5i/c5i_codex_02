# Repository guidance

## Purpose and public interface

This repository is a self-contained training lab about project instructions for Codex (`README.md`). The learner starter is a small Python checkout example. Its public function is `calculate_total(items)`, which returns a float for items with `price` and `quantity` fields (`learner/starter/README.md`, `learner/starter/src/checkout.py`).

## Working rules

- Read the relevant task card, source, and tests before changing the starter (`learner/starter/task_card.md`, `learner/starter/src/checkout.py`, `learner/starter/tests/test_checkout.py`).
- Preserve existing calls and the float return contract unless the task explicitly changes them (`learner/starter/src/checkout.py`, `learner/starter/task_card.md`).
- Keep formatting separate from calculation when working on Task B (`learner/starter/task_card.md`).
- Keep changes within the requested task; do not add dependencies or change the item schema for Task A (`learner/starter/task_card.md`).
- If a task is ambiguous or conflicts with the observed contract, state the uncertainty and ask for clarification before making a consequential choice. This is a cautious workflow recommendation; the repository does not specify an ambiguity policy.

## Verification

From `learner/starter/`, run:

```sh
python3 -m unittest discover -s tests -v
```

This is the verification command documented by the starter README; no package installation is required (`learner/starter/README.md`).

## Scope

The learner project lives in `learner/starter/`; lab instructions and templates live in `learner/` (`README.md`). Do not treat instructor materials described in the root README as learner-project source. Their presence is not confirmed in this checkout's listed files (`README.md`).
