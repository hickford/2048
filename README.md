# 2048

This is a fork of the game 2048, I changed the scoring algorithm to be more meaningful.

In the original game, score grew faster than the largest tile, and seemed to have to connection with the win condition. By the time the player created a 2048 tile, their score would typically be around 20,000. Most players ignored the score.

A better scoring algorithm would measure progress towards the goal of making a 2048 tile. It would have these properties:

1. Score ≥ 2048 is necessary and sufficient to win.
2. Score is bounded below by the largest tile on the grid, and above by the (yet unmade) tile beyond that.
3. Score is increasing.
4. Score is a function only of the current grid, and not how that grid was arrived at.
5. Intermediate scores between 1024 and 2048 are possible.

This suggests a new scoring algorithm: sum distinct tiles, allowing any duplicate to substitute for all smaller titles.

[Play the game here!](https://hickford.github.io/2048/).
