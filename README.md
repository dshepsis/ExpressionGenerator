# ExpressionGenerator

## Synopsis
This is a short script meant to generate test-cases for expression evaluators. Simply select the complexity (roughly determines expression length) and the number of expressions you wish to generate, then click "Generate".

## How it Works
It starts with a single random integer between 1 and 99 (inclusive). It will then iterate over the expression n times, where n is the "Complexity" chosen in the form in index.html.

For each iteration, the script randomly selects an operand in the expression, and applies a randomly chosen "transformation".

Each transformation involves replacing the given operand with another value, usually the operand followed by an operator, followed by another random operand. For example, "23" might become "23 * 11". Finally, there is a random chance that the result will also be surrounded by parentheses, e.g. "(23*11)".

The list of transforms is as follows, with "op" representing the operand to be replaced, and "ri" representing a random integer in between 1 and 99:

* op → op + ri
* op → op - ri
* op → ri - op
* op → op * ri
* op → op / ri
* op → ri / op
* op → op

Note that the last transformation doesn't change the expression. This is an "identity" transformation, and exists as a default if no other transformations are chosen. This also means that the length of an expression can vary significantly, even if the complexity remains constant.

## Link
You can view the full page <a href="https://dshepsis.github.io/ExpressionGenerator/">here</a>.
