# testing-with-jasmine
Unit testing JavaScript code with a JavaScript testing library called Jasmine

### Importance of Testing
* Writing tests for different functions or operations are healthy practice to keep small to major bugs away from your code.
* Usually with bigger code base, it is important to always unit test different features and operations to keep track of proper outcomes while coding.
* Writing unit tests gives you more confidence with your code and makes sure you are on the right path to acheieving your goal in your projects.
* Especially, if you have a team working on a project, it is crucial to unit test for you and others in your team to ensure and trust on each other's code.

### Essential Keywords
* describe - used to organize the test (literally describes the tests you are about to create)
* it - describes what you are expect a functionality to achieve (describes what the outcome of an operation should be based on given situation; "it" goes inside "describe" block)
* expect - what the actual technical outcome should be 

Quick look...

```js
	<!-- code -->
	let earth = {
		isRound: true,
		numberFromSun: 3
	};

	<!-- unit tests -->
	describe('Earth', () => {
		it('should be round', () => {
			expect(earth.isRound).toBe(true);
		})
		it('should be third planet from the sun', () => {
			expect(earth.numberFromSun).toBe(3);
		})
	})
```

### Matchers
* Use matchers to compare and contrast result value of an operation with the expected value
* __Popular matchers__:
	* toBe/not.toBe                	 // to check if the result value is === to the expected value
	* toBeCloseTo					 // to check if the result value is close to the expected value
	* toBeDefined					 // to check if the result value is not undefined
	* toBeFalsy/toBeTruthy			 // to check if the result value either a falsy or truthy value
	* toBeGreaterThan/toBeLessThan   // to compare if the result value is greater or less than expected value
	* toContain						 // used for arrays to check if an array contains all the items expected
	* toEqual						 // to check if the result value is === to the expected value and their references in memory match as well
* Refer to [Jasmine matchers](https://jasmine.github.io/api/2.8/matchers.html)

### Good Testing Practices
* Try to limit repititions inside tests to avoid cluttered code, instead put the repeated code inside "beforeEach" block to run the repeated code before each "it" callback function. Also, on the other hand, to run the repeated code after each "it" callback function, put the repeated code inside "afterEach" block.
* To break tests down into smaller suites for better understanding of each tests, we can use nested "describe" blocks. You can have as many nested blocks you want, but try not to have more than 2 nested blocks
* Also, if you want, you can have multiple expect functions within a "it" block if they all test for similar concerns. 

### Using Spies
* Use species to mock a function you already have inside your code to run test quickly
* For more info, refer to [Jasmine Spy](https://jasmine.github.io/api/2.8/Spy.html)

### Test Driven Development (TDD)
* Write your tests before your writing your application code
* Not the most widely used approach to testing
* __Process__:
	* write the tests
	* see all tests to fail
	* write code to pass the tests
	* refactor code as necessary

### Behavior Driven Development (BDD)
* A subset of Test Driven Development
* When writing tests, describe the behavior of operation testing, not just the value expected
* Helpful for testing software with design


### To Deal With Asynchronous Code
* Use either [Clock](https://jasmine.github.io/api/2.8/Clock.html) or by passing "done" function as a parameter to "it" callback

### Other Kinds of Tests
* Integration Tests (quite similar to unit testing)
* Acceptance Tests (performing tests on a full system)
* Stress Tests (tests for see how code will perform on unlikely or unfavorable situtations)


### Quick Reference
* [Jasmine Documentation](https://jasmine.github.io/)
* [Setup unit testing inside the browser with Jasmine]()
