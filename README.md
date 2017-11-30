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



### Quick Reference
* [Jasmine Documentation](https://jasmine.github.io/)
* [Setup unit testing inside the browser with Jasmine]()
