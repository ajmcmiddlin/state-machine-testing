# Property based testing

##

Specify properties that functions should have, and ensure they hold with random inputs.

##

```haskell
-- Reverse is involutive
propReverse :: Property
propReverse =
  property $ do



```

##

```haskell
-- Reverse is involutive
propReverse :: Property
propReverse =
  property $ do
    xs <- forAll $ Gen.list (Range.linear 0 100) Gen.alpha


```

##

```haskell
-- Reverse is involutive
propReverse :: Property
propReverse =
  property $ do
    xs <- forAll $ Gen.list (Range.linear 0 100) Gen.alpha
    reverse (reverse xs) === xs
```

## { data-background-image="images/phases.png"
      data-background-color="white"
      data-background-size="80%"
      data-background-transition="none"
    }

## {data-background-image="images/hedgehog.png" data-background-size="contain"}

