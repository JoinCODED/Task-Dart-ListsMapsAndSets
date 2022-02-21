### Lists

1. Your main method should look like this:

```dart
void main() {
  const values = [5, 3, 15, 4, 1];
}
```

2. Let's create a variable to store the sum of the elements:

```dart
void main() {
  const values = [5, 3, 15, 4, 1];
  int sum = 0;
}
```

3. Next, we will iterate over the list using a `for` loop:

```dart
void main() {
  const values = [5, 3, 15, 4, 1];
  int sum = 0;
    for (var value in values) {
  }
}
```

4. On every iteration we will add the `value` to the `sum` variable:

```dart
void main() {
  const values = [5, 3, 15, 4, 1];
  int sum = 0;
    for (var value in values) {
    sum = sum + value;
  }
}
```

5. And because we like shorter code:

```dart
void main() {
  const values = [5, 3, 15, 4, 1];
  int sum = 0;
    for (var value in values) {
    sum += value;
  }
}
```

6. Print the result:

```dart
void main() {
  const values = [5, 3, 15, 4, 1];
  int sum = 0;
    for (var value in values) {
    sum += value;
  }
  print(sum);
}
```

### Sets

1. Your main method should look like this:

```dart
void main() {
const a = { 3, 5 };
const b = { 5, 7 };
}
```

2. We need to join those to sets using the `union` method:

```dart
void main() {
const a = { 3, 5 };
const b = { 5, 7 };
final aAndB = a.union(b);
print(aAndB);
}
```

output:

```
{3, 5, 7}
```

3. Now we need to know which elements are in common between set `a` and set `b` and for that we use the `intersection` method:

```dart
void main() {
const a = { 3, 5 };
const b = { 5, 7 };
final aAndB = a.union(b);
final commonElements = a.intersection(b);
print(aAndB);
print(commonElements);
}
```

output:

```
{3, 5, 7}
{5}
```

4. Lastly, we will use the `difference` method to get the different elements between `aAndB` and `commonElement`:

```dart
void main() {
const a = { 3, 5 };
const b = { 5, 7 };
final aAndB = a.union(b);
final commonElements = a.intersection(b);
final differentElements = aAndB.difference(commonElements);
print(differentElements);
}
```

output:

```
{3, 7}
```

5. And of course we can chain our methods to make the code shorter:

```dart
void main() {
  const a = {1, 3};
  const b = {3, 5};
  final differentElements = a.union(b).difference(a.intersection(b));
  print(c);
}
```

### Maps

1. Your main method should look like this:

```dart
void main() {
const menu = {
  'burger': 6.5,
  'pizza': 5,
  'water': 1.5,
};
}
```

2. Let's create an order:

```dart
void main() {
    const menu = {
        'burger': 6.5,
        'pizza': 5,
        'water': 1.5,
    };
    const order = ['pizza', 'water'];
  }
```

3. Create a variable to store the total price:

```dart
double total = 0.0;
```

4. Using a `for` loop, iterate over the `order` list:

```dart
  for (var item in order) {
  }
```

5. To get the price of the item we access the `menu` map with the `[bracket]` notation:

```dart
  for (var item in order) {
      final price = menu[item];
  }
```

6. What if the item is not in the map? the `price` value will be `null`, so let's make an `if` condition to print the error message:

```dart
  for (var item in order) {
      final price = menu[item];
      if(price == null){
          print("$item is not on the menu");
      }
  }
```

7. Otherwise we want to add the `price` to our `total` variable:

```dart
  for (var item in order) {
      final price = menu[item];
      if(price == null){
          print("$item is not on the menu");
      } else {
          total += price;
      }
  }
```

8. After we are done iterating, we print the `total`:

```dart
void main() {
    const menu = {
        'burger': 6.5,
        'pizza': 5,
        'water': 1.5,
    };
    const order = ['pizza', 'water'];
    double total = 0.0;
  for (var item in order) {
      final price = menu[item];
      if(price == null){
          print("$item is not on the menu");
      } else {
          total += price;
      }
  }
    print(total);
  }
```
