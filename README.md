# Sphinx

Sphinx is a simple unit test framework for [Litan](https://github.com/JeneLitsch/Litan)

## How to use

Add your tests to the sphinx::test namespace.

```js
namespace sphinx::test {
	function test_something() {
		// Test stuff
	}
}
```

Use different asserts to test your code.

```js
namespace sphinx::test {
	function test_something() {
		assert_true(result); // Ok if result is true
		assert_false(result); // Ok if result is false
		assert_equal(a, b) // Ok if a and b are equal
		assert_equal_strict(a, b) // Ok if a and b are strictly equal
		assert_success(callable) // Ok if callable does not throw
		assert_except(callable) // Ok if callable does throw
	}
}
```

Run test from main.

```js
function main(args) {
	sphinx::run_tests();
}
```

Get your results

```
Results
Tests:       42
Total cases: 1337
Errors:      0
All tests successful :)
```