# What makes a good test?

* Group tests by class
  * It’s easier to see at a glance what your test coverage is this way, and it’s easier to keep test files small
  * I’d also suggest putting unit tests in a different directory than integration tests
* Write as little code as possible
  * Since tests should be grouped by class, there is probably some test setup they can share. Create instances/variables you can reuse
  * Test cases are great! If you need to test some logic with a series of different inputs and expectations, just add them as test cases instead of a whole separate test
  * Build test bases/helpers that can be shared between test classes for common setup
* BDD
  * I find behaviour driven development (BDD testing) a good way to make sure tests are readable and focus on what’s important, which is the behaviour of your application. They’re also a good way to bridge the gap between product people and code.
      * There are a couple of different popular BDD formats - I’m used to Given/When/Then, but I'm not partisan 
      * There are actual testing libraries which enforce your GWTs in code, if you want to be particularly rigorous
* Integration tests for end-to-end flows & places where there’s logic in the database, unit tests for business logic or code that calls 3rd parties
  * Getting a good mocking framework in place is a huge help when you want to test your business logic without necessarily reaching out to S3, putting records in the database, etc
    * Even for integration tests, it’s preferable to test against a separate test db
  * This has implications for how you write code as well - consider the testability of your production code
* One assert per test (where possible) and equivalence assertions
  * Having a principle of 1 assert per test forces you to be clear about what specifically you’re testing and discourages writing ‘god tests’ that are hard to read and maintain
  * Equivalence asserts are easier to read and provide more comprehensive assurance that your code does what you expect without side effects
* Good naming/general readability
  * Tests should have names that clearly & concisely reflect what they do and their variables should also
  * Reasonphrases on test failure are always nice for debugging! Most testing frameworks let you pass a string as a second argument to asserts that will be printed in case of failure
  * Consider extracting into a private method any code in a test that isn’t part of the functionality you’re verifying and exceeds a small number of lines (maybe ~4-6) - even if it’s not reused by other tests. It helps keep the focus on what’s important for a reader
