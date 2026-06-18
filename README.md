# Probs

<p align="center">
  <img src="icono.png" alt="Probs icon" width="96">
</p>

A browser-based probability calculator for draw scenarios involving white balls in a finite population. It supports common probability setups such as drawing with or without replacement, checking for exact or minimum successes, and estimating the chance of success across repeated attempts.

The interface is currently in Spanish.

## Features

- Calculates probabilities for drawing white balls from a population.
- Supports sampling with replacement and without replacement.
- Handles "at least `k` white balls" success conditions.
- Handles "exactly `k` white balls" success conditions.
- Includes an optional strict-order mode where the first `k` draws must be white.
- Supports repeated attempts using `1 - (1 - p)^j`.
- Displays the result as both a percentage and a "1 in X" estimate.
- Runs entirely client-side with no dependencies, build step, or backend.

## Probability Models

The calculator uses different models depending on the selected configuration:

- **Without replacement:** hypergeometric probability.
- **With replacement:** binomial probability.
- **Strict-order mode:** prefix probability, where the first `k` draws must be successful.
- **Repeated attempts:** cumulative probability across `j` independent attempts.

## Tech Stack

- HTML
- CSS
- JavaScript

## Running Locally

Clone the repository and open `index.html` in a browser:

```bash
git clone https://github.com/MarcosGibert/probs.git
cd probs
open index.html
```

You can also serve the folder locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## How It Works

Enter the total population size, the number of white balls, the sample size, and the target number of white balls. Then choose whether the draw is performed with replacement, whether the target should be exact or minimum, and whether order should matter.

After pressing **Calcular**, the app computes the probability for one attempt and, if multiple attempts are entered, converts it into the probability of succeeding at least once.

## Project Context

This was built as a small personal learning project to make probability scenarios easier to explore interactively. The goal is to turn abstract formulas into a simple interface where changing one value immediately changes the interpretation of the result.

