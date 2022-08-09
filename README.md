# Variables Lab

## Learning Goals

- Practice using `const` and `let` to declare variables in JavaScript

## Instructions

In this lab we'll practice declaring and assigning values to variables. We'll
also go over how to read the test document. Understanding how to read the tests
can be a valuable tool in figuring out exactly what you'll need to do to
complete the lab.

### Tests

When we want to run an experiment, we need to develop a hypothesis and we need
to test it. In programming, we run tests to verify that programs behave the way
we think they do. Tests help us identify bugs and judge how healthy our
applications are.

We use tests to describe the program's behavior, just as you would in a
professional coding environment, and we also use them as teaching tools. We will learn how to write our own tests in later modules, but for now you are
only in charge of getting given tests to pass.

### Structure

The structure of this lab — where its files and folders are located
— looks roughly like the following:

``` text
├── CONTRIBUTING.md
├── LICENSE.md
├── README.md
├── index.js
├── node_modules/
├── package.json
└── test
    └── indexTest.js
```

All labs will more or less have the same structure. (And non-lab lessons, for
that matter, will still have CONTRIBUTING.md, LICENSE.md, and README.md files.)

### Code Along

Open up `index.js` in your text editor; you should see, well, nothing. We'll fix
that soon.

Now open up `test/indexTest.js`. Hey, there's something! What's all of this
stuff doing?

**Note:** The `test/indexTest.js` has great info that we want to look at, but do
not edit this file otherwise you may have extra difficulty passing this lab.

A few lines down in the `test/indexTest.js` file you will see:

```js
describe('index.js', function () {
  // there's stuff in here, too
});
```

`describe` is a function provided by our test library, Mocha, and it's used to
hold our tests. After the word `describe` is information about our tests. Tests
are used as a way to document the behavior of a function to developers. For
example, the next word `describe` is followed by is the word `companyName`. Here
the test is telling us that the tests that come afterwards will be about
`companyName`. Then comes the word `it`, where you see the following:

```js
it('is set as Scuber', function () {
  // tests are here
});
```

This is telling us that the `companyName` should be set to `Scuber`. Finally,
filling in the missing part of the `it` code, we see:

```js
it('is set as Scuber', function () {
  expect(companyName).to.equal('Scuber');
});
```

This example shows that the test expects `companyName` to equal `Scuber`. That
`expect` and `to.equal` are essentially doing the same thing as `companyName ==
'Scuber'`. In other words, `expect(companyName).to.equal('Scuber')` is running
code that will have this first test pass if `companyName` equals `Scuber` and
fail if it does not.

Don't worry too much yet if it's hard to understand what is happening inside of
the `test/indexTest.js` file. But it's a good idea to open up the file, and
gather the information that you can. We will also provide instructions in the
`README.md` file that will allow you to complete the lab.

## Running the Tests

We learned how to run tests in **Completing Your First Software Engineering Assignment**, but it may take a few times before the process becomes comfortable. 
So, let's run through it again together. 

1. The first step is to install the required testing dependencies using `npm install`. 
  - As always, make sure you are in the root directory of the cloned lab when running this command.
2. The second step is to run the test using `npm test`.

You should now see the current status of the tests in the terminal. For the moment, 
all of the tests fail. Let's figure out how to get one of them passing! (The rest will be up to you.)

To get our first test to pass, we can open up our `index.js` file, and write the
following:

```js
let companyName = 'Scuber';
```

If you run `npm test` again, you'll see that our first test is now passing.
However, the second test, which is also about `companyName`, is not yet passing.
It's not passing because it expects `companyName` to be declared using a
different keyword than the `let` keyword — it needs a keyword that is used for
variables that can't be changed... can you remember what that is?

Continue to work through the problems below. Keep in mind the general workflow
for a lab:

1. Run `npm test`.
2. Read the errors; vocalize what they're asking you to do.
3. Write code; repeat steps 1 and 2 often until a test passes.
4. Repeat as needed until all the tests are passing.

## Working Through the Problems

If you open up `test/indexTest.js`, you will see all the tasks in front
of you. We recommend attempting to read the tests to figure out what is 
asked of you. 

To review what we did together, recall that we looked at the `describe`
function call for the `companyName` variable. This is how we knew we 
needed a variable named `companyName`. 

Then, we saw there are two `it` function calls inside this `describe` 
function. The first one says it expects the variable `companyName` to be 
set as Scuber. To pass this, we went into `index.js` and wrote the line 
`let companyName = 'Scuber'`. 

The second `it` function call says it expects `companyName` to be defined 
as a `const`. To pass this, you should again go into your `index.js` and make sure you are using the correct type of variable declaration for this 
particular variable.

The remaining tests follow the same structure, where it checks for a 
variable to be defined with a certain value and declaration. Try reading
through them and passing them by writing code in `index.js` to complete 
the lab. 

<details>
<summary>Expand this dropdown for more guidance or to check if you're reading the tests correctly</summary>

  - `companyName` 
    - Should be set to `Scuber`
    - Should be defined as a `const` 
  - `mostProfitableNeighborhood`
    - Should be set to `Chelsea`
    - Should be defined using `let`
  - `companyCeo`
    - Should be set to `Susan Smith`
    - Should be defined using `let`
</details>

## Submitting the Assignment

Similar to running tests, we also learned how to submit assignments in the
**Completing Your First Software Engineering Assigmnent**. In case you forget how to run tests or submit assignments for any labs going forward, that assignment is a good one to refresh your memory. 

For this lab, though, we will quickly run through the steps together.

1. Track all the work you did for the lab using `git add -A`.
  - Again, make sure you are in the root directory of the cloned lab when running this command.
2. Save all the work you just tracked using `git commit -m "some message here"` 
  - Be sure your message is informative but succint, for example "complete lab".
3. Push all the work you tracked and save to your forked version of the lab on GitHub using `git push origin main` 

Now if you check your forked version on GitHub, you should see all the work you did online. 

> **NOTE**: You can run the above three steps as often as you would like when working on labs and code projects in general. In fact, it is good practice to commit often whenever you complete a milestone rather than only one time at the end when you complete an entire project. We will learn more about this and git at the end of this module.  

Once you've passed all tests and pushed all your work onto your GitHub fork, you should then:

1. Copy the link for your GitHub fork of the lab.
  - Check the link to make sure you see **your** username. If it's not there, you are _not_ copying your forked version.
2. Go back to the Canvas assignment for this lab and click the **Start Assignment** button at the top. 
3. Paste in the copied link into the Website URL box and hit submit.

With that, you've completed your first JavaScript assignment!

## Resources

- [MDN: Let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)
- [MDN: Const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
