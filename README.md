# Custom Jeopardy

Build custom Jeopardy games.

The schema is:

```
{
  single: Array<Category>;
  double: Array<Category>;
  final: Category;
}
```

```
interface Category {
  // Name of the category.
  name: string;
  // A comment for the category.
  comment: string;
  // An array of clues.
  clues: Array<Clue>;
}

interface Clue {
  // The monetary value of the clue. Use NaN for daily doubles.
  value: number;
  isDailyDouble: boolean;
  text: string;
  answer: string;
}
```
