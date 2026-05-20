# Lab 7

## Group Members: Ryan Dang

## Check your Understading: 1) Where would you fit your automated tests in your Recipe project development pipeline?

Within a GitHub Action that runs whenever code is pushed.

Running automated tests in a GitHub Action on every push catches bugs early and progressively, before it is merged to main. The tests run in a consistent environment every time, so results do not depend on one developer remembering to run them locally. Waiting until all development is finished to start testing could result in diasaterous consequences since major code-breaking bugs can pass through unnoticed during the dvelopement progess.

## Check your Understanding: 2) Would you use an end to end test to check if a function is returning the correct output?

No, I would not. End-to-end tests automate full user flows through the browser. Checking whether a single function returns the correct value is a is a problem that can be solved with unit-testing, where we can call the function directly with inputs and assert on the return value, without launching a browser or simulating UI actions.

