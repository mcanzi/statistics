# Statistics

Slides and tutorials for Statistics (Dr Massimiliano Canzi, Department of Linguistics, University of Konstanz), an introduction to data analysis in R for MA students in linguistics. The course runs from the tidyverse and descriptive statistics to linear models, interactions, significance testing, mixed models (`lme4`) and mixed-effects logistic regression. The lectures follow **Winter (2019)**, *Statistics for Linguists: An Introduction Using R* (Routledge). All of the examples and exercise sheets use simulated linguistic data from the [`simling`](https://github.com/mcanzi) package.

| | Lecture | Winter (2019) |
|---|---|---|
| 1 | Course introduction | 1 |
| 2 | Data wrangling | 2 |
| 3 | Descriptive statistics | 3 |
| 4 | Linear models | 4 |
| 5 | Transformations | 5 |
| 6 | Multiple regression | 6 |
| 7 | Categorical predictors | 7 |
| 8 | Interactions | 8 |
| 9 | Significance testing | 9 |
| 10 | Mixed models 1 | 14 |
| 11 | Mixed models 2 | 15 |
| 12 | Mixed logistic regression | 12, 15.8 |
| 13 | Power and model building | 10, 11, 16 |

The slides are online at [mcanzi.de/statistics](https://mcanzi.de/statistics/01_course_introduction.html).

## Rendering the slides

The lectures are [Quarto](https://quarto.org) revealjs decks (`source/*.qmd`). Run `quarto render` in `source` to render every lecture into `docs`, which GitHub Pages serves; `quarto render 04_linear_models.qmd`, or the Render button in RStudio, renders a single one. The options all lectures share (slide size, transitions, chunk defaults) are in `source/_quarto.yml`; each lecture's YAML has only its title, subtitle and footer, and the few options in which it differs. All lectures use the forest theme of mcanzi.de (`source/forest.scss`): green-black, leaf green and moon yellow, with rafflesias drawn in ink in the background. `source/slides_setup.R` sets the plot colours to match it. The fonts are in `source/fonts` (declared in `source/fonts.css`) and are embedded in each HTML file, so every deck is a single file that works offline.

Requires [Quarto](https://quarto.org) (bundled with RStudio), `tidyverse`, `revealjs` (tutorial slides), `palmerpenguins`, `simling`, `broom`, `lme4`, `lmerTest` and `effsize`; optional: `qrcode` (QR codes), `ragg` and `systemfonts` (Atkinson Hyperlegible in the figures).

## Tutorials

Each tutorial is one file with its solutions in `source/tutorials`, named like its lecture (`03_descriptive_statistics.Rmd`). Tutorial 1 is a guided tutorial, which I go through with the class: installing konstats, a first look at simling, and the R basics of lecture 1. Its .Rmd keeps all the code (`guided: true` in its YAML header). Every solution sits in a `::: solution` block. Tutorials 2, 4, 8, 10 and 12 end with a weekly assignment in a box, and lecture 13 has no tutorial. The weekly assignment never has solutions in these files (rendering stops if it finds one), so tutorials can be published at any time. Knit `source/render_tutorials.Rmd` to make two versions of each tutorial in `docs/tutorials`:

- `03_descriptive_statistics.Rmd`, the exercise sheet for students: the same file without the solutions, with an empty chunk where each piece of solution code was. It knits to a plain page with the `darkly` theme.
- `03_descriptive_statistics.html`, the slides: the lecture theme, one exercise at a time, each followed by its solution.

`render_tutorials.Rmd` explains how solution blocks and slide breaks work. The teaching page of mcanzi.de links each tutorial's slides and exercise sheet.

| | Tutorial | Slides | Exercise sheet |
|---|---|---|---|
| 1 | Getting started (guided) | [01_getting_started.html](https://mcanzi.de/statistics/tutorials/01_getting_started.html) | [01_getting_started.Rmd](https://mcanzi.de/statistics/tutorials/01_getting_started.Rmd) |
| 2 | Data wrangling | [02_data_wrangling.html](https://mcanzi.de/statistics/tutorials/02_data_wrangling.html) | [02_data_wrangling.Rmd](https://mcanzi.de/statistics/tutorials/02_data_wrangling.Rmd) |
| 3 | Descriptive statistics | [03_descriptive_statistics.html](https://mcanzi.de/statistics/tutorials/03_descriptive_statistics.html) | [03_descriptive_statistics.Rmd](https://mcanzi.de/statistics/tutorials/03_descriptive_statistics.Rmd) |
| 4 | Linear models | [04_linear_models.html](https://mcanzi.de/statistics/tutorials/04_linear_models.html) | [04_linear_models.Rmd](https://mcanzi.de/statistics/tutorials/04_linear_models.Rmd) |
| 5 | Transformations | [05_transformations.html](https://mcanzi.de/statistics/tutorials/05_transformations.html) | [05_transformations.Rmd](https://mcanzi.de/statistics/tutorials/05_transformations.Rmd) |
| 6 | Multiple regression | [06_multiple_regression.html](https://mcanzi.de/statistics/tutorials/06_multiple_regression.html) | [06_multiple_regression.Rmd](https://mcanzi.de/statistics/tutorials/06_multiple_regression.Rmd) |
| 7 | Categorical predictors | [07_categorical_predictors.html](https://mcanzi.de/statistics/tutorials/07_categorical_predictors.html) | [07_categorical_predictors.Rmd](https://mcanzi.de/statistics/tutorials/07_categorical_predictors.Rmd) |
| 8 | Interactions | [08_interactions.html](https://mcanzi.de/statistics/tutorials/08_interactions.html) | [08_interactions.Rmd](https://mcanzi.de/statistics/tutorials/08_interactions.Rmd) |
| 9 | Significance testing | [09_significance_testing.html](https://mcanzi.de/statistics/tutorials/09_significance_testing.html) | [09_significance_testing.Rmd](https://mcanzi.de/statistics/tutorials/09_significance_testing.Rmd) |
| 10 | Mixed models 1 | [10_mixed_models_1.html](https://mcanzi.de/statistics/tutorials/10_mixed_models_1.html) | [10_mixed_models_1.Rmd](https://mcanzi.de/statistics/tutorials/10_mixed_models_1.Rmd) |
| 11 | Mixed models 2 | [11_mixed_models_2.html](https://mcanzi.de/statistics/tutorials/11_mixed_models_2.html) | [11_mixed_models_2.Rmd](https://mcanzi.de/statistics/tutorials/11_mixed_models_2.Rmd) |
| 12 | Mixed logistic regression | [12_logistic_regression.html](https://mcanzi.de/statistics/tutorials/12_logistic_regression.html) | [12_logistic_regression.Rmd](https://mcanzi.de/statistics/tutorials/12_logistic_regression.Rmd) |

## License

Course materials © Massimiliano Canzi, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (see `LICENSE.md`). Code is licensed under the MIT License (see `LICENSE-CODE.md`). The fonts used in the slide theme (Atkinson Hyperlegible, Bricolage Grotesque, JetBrains Mono) are licensed under the SIL Open Font License 1.1 (see `source/fonts/OFL-*.txt`).
