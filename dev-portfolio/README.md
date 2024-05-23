# Personal Portfolio

## Get started

```
npm i && npm run dev
```

## About repo

-   Using NextJs
-   React
-   Styled components (each component has a corresponding ComponentStyles.js file)

## Testing

### visual testing

For visual testing I had to enable an [ignore threhold](https://docs.happo.io/docs/compare-threshold)

How do we test all of the urls in our app?

What about timelineData.js, do we need to write a snapshot test for it?

-   No, since the data appears in our visual tests, it's not necessary

-   Disable running all of the cypress files for visual tests by using [Cypress --spec](https://docs.cypress.io/guides/guides/command-line#cypress-run)

### functional testing

-   how do we test the links in Projects.js?

### front-end perf

`cy.lighthouse(), Electron is not supported. Skipping...` error was a result of running Cypress on Electron. Changing to Chrome browser fixed the issue.

### updating npm packages

Use [npm-check](https://koalatea.io/how-to-update-all-your-npm-packages-at-once)
