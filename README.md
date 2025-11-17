# MSCS532_Assignment5

This repository contains two QuickSort implementations used for performance comparison in an algorithms assignment:

- `randomQuickSort.py`: randomized quicksort (chooses a random pivot)
- `deterministicQuickSort.py`: deterministic quicksort using median-of-three pivot selection

Each script includes a `generate_number_list(n, list_type)` helper and a `__main__` section that generates four large lists (ascending, descending, random, duplicates) of 1,000,000 elements and times the sorting run.

How to run (PowerShell)

Run either implementation directly with Python from the repository folder:

```
python .\deterministicQuickSort.py
python .\randomQuickSort.py
```

Notes and tips

- The scripts create lists of 1,000,000 elements by default which can be very slow or memory intensive on some machines. For quick testing, open the script and reduce the value passed to `generate_number_list` in the `if __name__ == "__main__"` block (for example, use `10000` instead of `1000000`).
- If you want to run programmatic tests instead of the built-in benchmark, import the functions in a REPL or small wrapper script and call `generate_number_list` and `quicksort`/`random_quicksort` with smaller sizes.

Example quick test (PowerShell):

```
python -c "from deterministicQuickSort import generate_number_list, quicksort; a=generate_number_list(10000,'random'); print(len(quicksort(a)))"
```