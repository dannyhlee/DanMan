## Cats

### Foldable 

data structures that can be *folded* to a summary value

FOLDLEFT - eager left-associative fold

FOLDRIGHT - lazy right-associative fold

FOLD (combineAll) - combines every value

FOLDMAP - maps every `A` value into `B` then combines.
```
Foldable[List].foldMap(List("a", "b", "c"))(_.length)
res0: Int = 3
```

FOLDK - similar to fold, but combines every value using MonoidK[G] instead of Monoid[G]
```
Foldable[List].foldK(List(List(1, 2), List(3, 4, 5)))
res0: List[Int] = List(1, 2, 3, 4, 5)
```

FIND - returns Option of first element that matches predicate
```
Foldable[List].find(List(1, 2, 3))(_ > 2) should be(Some(3))
```

EXISTS - boolean for a predicate

FORALL - checks if all ele satisfy predicate

TOLIST - convert F[A] to List[A]

FILTER_ - convert F[A] to List[A] that match predicate
```
Foldable[List].filter_(List(1, 2, 3))(_ < 3) should be(List(1,2))
```

TRAVERSE_ - traverse a foldable mapping, combine them using Applicative[G] and discard results, returning Some() or None.
```
import cats.implicits._

def parseInt(s: String): Option[Int] =
  Either.catchOnly[NumberFormatException](s.toInt).toOption

Foldable[List].traverse_(List("1", "2", "3"))(parseInt) should be(Some(()))
Foldable[List].traverse_(List("a", "b", "c"))(parseInt) should be(None)
```





