# Cypress

An example project using the automation tool, [Cypress](https://www.cypress.io/). These tests are intended to provide examples of common actions you may need in your testing. I've included:
- page objects
- various ways of running the tests (via npm scripts)

## Requires
1. [node](https://nodejs.org/en/)
1. [git](https://git-scm.com/)

## Setup
1. clone: `git@gitlab.com:satteam/cypress.git`
1. install: `npm i`

## Run Them Tests
1. all tests: `npm test`
1. just homePage: `npm run home`
1. headless: `npm run headless`
1. particular test: `npm run cy run -- --spec <path of spec file> -q --headed`. 
Ex: `npm run cy run -- --spec specs/searchSpec.js -q --headed`
Remove `-q --headed` for running particular test in headless mode.
---

## Some limitation
Cypress is an _agressively_ opinionated framework... some of these opinions are at best, misguided :) YMMV. I know it's very popular... but honestly, **I would avoid Cypress if you can**. My issues with Cypress include:

1. it's overly complex
1. TONS of misinformation about how to use it on the internets
1. it cannot handle new windows/tabs
1. it can't handle multiple domains in one test file
1. it requires learning a proprietary framework rather than learning to code
1. it teaches some bad testing habits (eg. expects in page objects)
1. it's slow
1. anything it doesn't handle the docs will tell you _YOU SHOULDN'T WANT TO DO THAT_ (eg. test if an element exists)
1. it's a total pain to get it working on CI
1. I have yet to see _anyone_ use it well