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
professional coding environment, and we also use them as teaching tools. You are
in charge of getting the tests to pass.

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

## Running the Tests

We learned how to run tests in **Completing Your First Software Engineering Assignment**, but it may take a few times before the process becomes comfortable. 
So, let's run through it again together. 

1. The first step is to install the required testing dependencies using `npm install`. 
  - As always, make sure you are in the root directory of the cloned lab when running this command.
2. The second step is to run the test using `npm test`.

You should now see the current status of the tests in the terminal. For the moment, 
all of the tests fail. Let's figure out how to get one of them passing! (The rest will be up to you.)

### Code Along 

Running `npm test` gives us a lot of information about the lab's tasks. If you scroll up to the top of the test output, you should see a list like so: 

```sh
index.js
  companyName
    1) is set as Scuber
    2) is defined as a const
  mostProfitableNeighborhood
    3) is declared as equal to Chelsea
    4) is defined using let
  companyCeo
    5) is declared as equal to Susan Smith
    6) is defined using let
```

The `index.js` informs us what file it expects all these tests to pass in. Underneath that we see three main headers: `companyName`, `mostProfitableNeighborhood` and `companyCeo`. Then under each header, there are numbered bullet points. These are the actual tasks being tested. 

Let's go through the first task together. 

The first task is listed under `companyName` saying it should be set as Scuber. With that, we can assume that `companyName` is the expected variable name and `Scuber` is the expected definition. 

Earlier, we saw that these tests will be applied to `index.js`, so let's open up the `index.js` file. In there, we can declare the `companyName` variable like so:

`let companyName = 'Scuber'` 

Now if you run `npm test` again, you'll see that our first test is  passing.
However, the second test, which is also about `companyName`, is not yet passing.
It's not passing because it expects `companyName` to be declared using a
different keyword than the `let` keyword — it needs a keyword that is used for
variables that can't be changed... can you remember what that is?

Continue to work through the problems until all tests pass. Keep in mind the general workflow
for a lab:

1. Run `npm test`.
2. Read the errors; vocalize what they're asking you to do.
3. Write code; repeat steps 1 and 2 often until a test passes.
4. Repeat as needed until all the tests are passing.

## The Problems

As we saw above when running `npm test`, the tasks for you to complete in `index.js` are to define the following variables: 

- `companyName` 
  - Should be set to `Scuber`
  - Should be defined as a `const` 
- `mostProfitableNeighborhood`
  - Should be set to `Chelsea`
  - Should be defined using `let`
- `companyCeo`
  - Should be set to `Susan Smith`
  - Should be defined using `let`

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
