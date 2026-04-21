# GeneticAlgorithmSuperMario
Python project that uses a Genetic Algorithm (GA) to train an agent to play Super Mario Bros. The algorithm evolves a population of agents over generations, improving their performance through selection, crossover, and mutation.

# Prerequisites

```bash
pip install gym gym-super-mario-bros nes-py numpy torch
```

## Training

In `main.py`, uncomment `main()` and comment out `test_best_model()` at the bottom:

```python
if __name__ == "__main__":
    main()
    # test_best_model()
```

Then run:

```bash
python main.py
```

The best model from each generation is automatically saved to `models/` as a `.npy` file. Training metrics are logged to `logs/training_log.csv`.

## Testing the Best Model

Switch the entry point to `test_best_model()`:

```python
if __name__ == "__main__":
    # main()
    test_best_model()
```

This loads the latest saved model and runs it with rendering enabled, printing the final score, x-position, fitness, and whether the flag was captured.
