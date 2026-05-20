# Lab 7

## Group Members: Ryan Dang

## Check your Understading: 1) Where would you fit your automated tests in your Recipe project development pipeline?

Within a GitHub Action that runs whenever code is pushed.

Running automated tests in a GitHub Action on every push catches bugs early and progressively, before it is merged to main. The tests run in a consistent environment every time, so results do not depend on one developer remembering to run them locally. Waiting until all development is finished to start testing could result in diasaterous consequences since major code-breaking bugs can pass through unnoticed during the dvelopement progess.

## Check your Understanding: 2) Would you use an end to end test to check if a function is returning the correct output?

No, I would not. End-to-end tests automate full user flows through the browser. Checking whether a single function returns the correct value is a is a problem that can be solved with unit-testing, where we can call the function directly with inputs and assert on the return value, without launching a browser or simulating UI actions.

## Check your Understanding: 3) What is the difference between navigation and snapshot mode?

Navigation mode audits the page as it loads from a fresh navigation like a user opening the URL. It measures load-time performance and runs checks during/after that load. It does not analyze interactions that happen later, such as clicking "Add to Cart."

On the other hand, Snapshot mode audits the page in whatever state it is in at the current moment. It is useful for catching issues in the current DOM but it cannot measure JavaScript performance over time or how the page changes after user actions.

## Check your Understanding: 4) Name three things we could do to improve the CSE 110 shop site based on the Lighthouse results.

1. Add a `lang` attribute to `<html>` — Lighthouse flagged that the document has no `[lang]` attribute under Accessibility (score 90). Adding something like `<html lang="en">` helps screen readers and browsers interpret the page language correctly.

2. Add a meta description — Under SEO (score 91), Lighthouse reported "Document does not have a meta description." Adding a `<meta name="description" content="...">` in the `<head>` would improve how search engines summarize the shop in results.

3. Use more efficient cache lifetimes — Even with a Performance score of 100, Lighthouse suggested "Use efficient cache lifetimes" (estimated savings of 10 KiB). Setting longer cache headers for static assets like CSS, JS, and images would help repeat visits load faster.

