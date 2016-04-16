# TDD

Always call out these phases intentionally.

AAA/GWT

1. Arrange - Given - Set stuffs up
2. Act - When - Invoke things
3. Assert - Then - Verify behaviors

AAA/GWT conscious tests:

* Are easier to read
* Point out potentially superfluous test code
* Can highlight certain test design smells

If you have many "Given" steps, maybe you have too many dependencies or complex arguments.

If you have many "When" steps, is the API confusing and hard or awkward to invoke?

If you have many "Then" steps, then you code is doing too much and is complex.

* Getting good value from tests requires clarity of intention and knowing what, when, and how to test.
* Write tests as if you expect your future self to have amnesia. Remember that you will forget; write tests that remind you of the story you once have.
* Novices often write code that is far too coupled; they combine unrelated responsibilities and bind many dependencies into every object.
* The complex code is usually written by the least qualified person. Novice programmers don't yet have the skills to write simple code.
* Tests provide documentation about the object under test. They tell a story about how it expects to interact with the world at large.
* Ignore testing messages sent to self.
* Ignore outgoing query messages.

---

In term of doing TDD, look at your Quality Problem. If it is not worth the trouble to up-keep the quality, then it is not worth to write tests as it will definitely slow development.

The reason to test is a new behaviour or new use-case, not because of a new method on a class.

* Override `Net::HTTP#start` to make sure it's never called by any test, because testing through network is slow and wrong.
* [Rails testing anti-patterns: Models](https://semaphoreapp.com/blog/2014/01/21/rails-testing-antipatterns-models.html)
* [Rails testing anti-patterns: Controllers](https://semaphoreapp.com/blog/2014/02/11/rails-testing-antipatterns-controllers.html)
* [Managing externals in Ruby tests](https://semaphoreapp.com/blog/2014/03/18/managing-externals-in-ruby-tests.html)
* [TDD Anti-patterns: The free ride](https://semaphoreapp.com/blog/2014/06/24/tdd-antipatterns-the-free-ride.html)
* [Setup tests with services](http://blog.arkency.com/2014/06/setup-your-tests-with-services/)
* [5 questions every unit test must answer](https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d)

There is no need for TDD for spiking or proof-of-concept coding.

* `E` - Syntax and runtime errors
* `F` - Assertion failures

## Why TDD

One reason: Refactoring! It will be faster to refactor once you have your passing tests. Refactoring is where DESIGN happens. To get to the design parts, write more tests. Making one test pass often points the way to the next test.

It is faster to run multiple verifications of your code as an automated test than to always check manually.

The tests act as a client for the entire code base, guiding all the code to have clean interactions.

The tests are the **source of truth** and are guiding the structure of the code.

The tests may pass, but it is not acceptable to the customer, i.e. it failed the acceptance tests.

## Is TDD Dead?

* [Martin Fowler's Is TDD Dead links](http://martinfowler.com/articles/is-tdd-dead/)
* [Test isolation is about avoiding mocks](https://www.destroyallsoftware.com/blog/2014/test-isolation-is-about-avoiding-mocks)
* [Hexagonal Rails and the ludicrous terminal application](http://pivotallabs.com/hexagonal-rails-and-the-ludicrous-terminal-application/)
* [Mocking and Ruby](http://solnic.eu/2014/05/22/mocking-and-ruby.html)

## Balance

Don't blindly create too many test cases. Never write a test that you expect to pass before writing more code, as it is a waste of time and test cases. It does not **drive code changes**.

You lose some of the benefit of TDD by creating too many test cases that don't drive code changes.

Make a list of test cases before you start writing the tests - that way you'll remember to cover all the **interesting cases**.

## Where to start?

* Initiation state
* Methods under test
* Happy path - What you want a successful interaction of the feature to look like.

Given - When - Then

Often, the best place to start is with a test that describes an initial state of the system, without invoking logic. This is especially useful if you are test driving a new class, so the first test just sets up the class and verifies the initial state of instance variables.

Next, determine the main cases that drive the new logic. The goal is to make the test pass quickly without worrying too much about niceties of implementation. Once test passes, look for opportunities to refactor.

When the main cases are done, what you try to do then is think of ways to break the existing code.

Refactoring is where design happens in a TDD process, and it's easiest to do in small steps. Skip at your peril.

At the most abstract level, you are looking for 3 things:

* Complexity to break up
* Duplication to combine. Duplication of fact/logic/structure
* Abstractions waiting to be born

## Refactoring

* Create method for compound booleans like `has_purchased_before?`
* 

## Behavior, not implementation

```
test "a completed task is complete" do
  task = Task.new
  refute(task.complete?)
  task.complete!
  assert(task.complete?)
end
```

Here, we let the message/method do the taking. We are not relying on our intimate knowledge of how to complete a task affect the test.

## Case Studies

* When a staff has resigned and took leaves, the "who-is-on-leave" email still include that staff. No test or edge case study was done on that. If we've written the test, we would have slow down and think of edge cases.

## Minitest

* [Getting started with Minitest](https://semaphoreci.com/community/tutorials/getting-started-with-minitest)
* [Shared example in Minitest is just Ruby](https://canaryup.com/blog/shared-examples-with-minitest)
* [Exception handling and testing it with Minitest](http://eftimov.net/exception-handling-and-testing/)
* [minitest-given](https://github.com/blowmage/minitest-given)
* [Minitest Let() is Lazy](http://ruby-journal.com/minitest-let-is-lazy/)
* [Minimalicious testing in Ruby 1.9 with Minitest](http://blog.arvidandersson.se/2012/03/28/minimalicous-testing-in-ruby-1-9)

## RSpec

* [Mixing and matching RSpec and Minitest](http://myronmars.to/n/dev-blog/2012/07/mixing-and-matching-parts-of-rspec)
* [New `expect` syntax since 2012](http://myronmars.to/n/dev-blog/2012/06/rspecs-new-expectation-syntax)
* [rspec-set](https://github.com/pcreux/rspec-set)
* [How RSpec works](http://interblah.net/how-rspec-works)

## Factories

* [Rails testing anti-patterns: fixtures and factories](https://semaphoreapp.com/blog/2014/01/14/rails-testing-antipatterns-fixtures-and-factories.html)

Factories are slow! They're slow by design.

## Mocks

A mock might be used:

* when the real object is unavailable
* difficult to access from a test environment

Verify the behavior of the system during the test, rather than the state of the system at the end of the test.

* stub - passive and you can don't call it in your test
* mock - aggressive and you must call it in your test or expectation error
* spy - just a stub where you need to expect later. Some people like spy more than mock because they can explicitly tell what behavior is being tested for. Spies are more consistent with the Given/When/Then test structure.

Avoid stubbing ActiveRecord's `find` method because it's part of an external library. Instead create a model method and stub that. Don't mock what you don't own.

## Videos

* [Jim Weirich on Decoupling from Rails](https://www.youtube.com/watch?v=tg5RFeSfBM4)
* [Sandi Metz The Magic Tricks of Testing](http://www.youtube.com/watch?v=URSWYvyc42M)