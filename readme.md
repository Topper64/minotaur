# Theseus and the Minotaur

A playable version of the "Theseus and the Minotaur" puzzle in the book *Mad
Mazes* by Robert Abbott.

## The Labyrinth

```
┏━━━━━━━━━┳━━━━━━━┳━━━━━━━━━┓
┃         ┃       ┃         ┃
┣━┳━┓ ╻ ╻ ┃ ┏━╸ ╺━┻━╸ ┏━━━╸ ┗━━
┃ ┃ ┃ ┃ ┃ ┃ ┃         ┃       →
┃ ╹ ╹ ┗━┛ ╹ ┗━╸ ━━━━━━┻━━━╸ ┏━━
┃                           ┃
┃ ╻ ┏━╸ ╻ ╻ ━━╸ ╻ ╻ ╺━━━╸ ╻ ┃
┃ ┃ ┃   ┃ ┃     ┃ ┃       ┃ ┃
┃ ┃ ┣━╸ ┃ ┃ ┃ ┃ ┃ ┗━━━━━┓ ┃ ┃
┃T┃ ┃   ┃ ┃ ┃ ┃ ┃       ┃ ┃M┃
┃ ┃ ┃ ╻ ╹ ┃ ┃ ╹ ╹ ╺━━━╸ ┃ ┃ ┃
┃ ┃ ┃ ┃   ┃ ┃           ┃ ┃ ┃
┃ ┃ ┃ ┃ ╻ ┃ ┃ ╻ ╻ ╺━━━╸ ┃ ┃ ┃
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃       ┃ ┃ ┃
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ╺━━━╸ ┃ ┃ ┃
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃       ┃ ┃ ┃
┃ ╹ ╹ ╹ ╹ ╹ ╹ ╹ ╹ ╺━━━╸ ╹ ╹ ┃
┃                           ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━┛
```

## Rules

On each turn, first Theseus may move one square vertically or horizontally, or
choose to not move at all.  Then, the Minotaur makes up to two moves.

The Minotaur always knows where Theseus is, and always tries to move towards
him.  However, it will prioritise matching Theseus's horizontal position, even
if there is a wall in the way that prevents the movement.

For example, consider the following situation:

```
┏━╸ ╺━┻
┃  M
┗━╸ ━━━
   T
━━╸ ╻ ╻
```

If Theseus were to move down, the Minotaur would simply take two steps down and
immediately catch him.  However, if Theseus were to move right, the Minotaur
would also move right, and then be unable to make a second move, even though
moving down then right would reach Theseus.

There is essentially only one solution, up to Theseus taking different routes
while the Minotaur is trapped behind a wall.
