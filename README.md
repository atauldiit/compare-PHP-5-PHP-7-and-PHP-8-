Let’s **compare PHP 5, PHP 7, and PHP 8** through an example that demonstrates how each version **handles arrays**, specifically focusing on new features and improvements introduced in each version.

**PHP 5**

In PHP 5, arrays are fundamental but lack some of the syntactic sugar introduced in later versions.

// PHP 5 - Basic array syntax
$fruits = array("apple", "banana", "cherry");

foreach ($fruits as $fruit) {
 echo $fruit . "\n";
}

**PHP 7**

PHP 7 didn’t introduce major changes to arrays directly, but its improved engine and new operators can affect how arrays are used.

// PHP 7 - Using the Spaceship Operator (for comparison within usort)
$numbers = [3, 2, 5, 6, 1];

usort($numbers, function($a, $b) {
 return $a <=> $b; // This is the Spaceship Operator
});

print_r($numbers);

**PHP 8**

PHP 8 introduced named arguments and attributes, which can be used with arrays, although it didn’t change the basic array structure.

// PHP 8 - Named arguments with arrays
function getFruitInfo(array $fruits, string $key) {
 return $fruits[$key] ?? 'Unknown fruit';
}

$fruits = ['apple' => 'green', 'banana' => 'yellow'];
echo getFruitInfo(fruits: $fruits, key: 'apple');
