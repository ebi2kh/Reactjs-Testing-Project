# react-web-app

Three React web app that is built with testing in mind

---

## react-web-app

### Install stuff

```bash
npm init -y
npm i create-react-app
npx create-react-app my-app
cd my-app
npm start
```

### 🧪️Testing strategy

| Expected Behavior                       | Tested? | Test Type | Technologies |
| --------------------------------------- | ------- | --------- | ------------ |
| A URL with the right text exists        | 🙅‍♂️      |           |              |
| App renders correctly                   | 🙅‍♂️      |           |              |
| URL is correct                          | 🙅‍♂️      |           |              |
| App looks as expected on web and mobile | 🙅‍♂️      |           |              |
| Front-end performance is at least a B   | 🙅‍♂️      |           |              |
| App is secure                           | 🙅‍♂️      |           |              |
| App is accessibility friendly           | 🙅‍♂️      |           |              |

### Run the tests that come with our app

- In a new terminal `npm run test`

### Add another test

| Expected Behavior                       | Tested? | Test Type | Technologies                |
| --------------------------------------- | ------- | --------- | --------------------------- |
| A URL with the right text exists        | ✅      | Component | React testing library, Jest |
| App renders correctly                   | 🙅‍♂️      |           |                             |
| URL is correct                          | 🙅‍♂️      |           |                             |
| App looks as expected on web and mobile | 🙅‍♂️      |           |                             |
| Front-end performance is at least a B   | 🙅‍♂️      |           |                             |
| App is secure                           | 🙅‍♂️      |           |                             |
| App is accessibility friendly           | 🙅‍♂️      |           |                             |

- Add a test for checking that the url is correct
- Update the url text
- Update the code to use a test id

### Shift-right and add a visual test

| Expected Behavior                       | Tested? | Test Type | Technologies                |
| --------------------------------------- | ------- | --------- | --------------------------- |
| A URL with the right text exists        | ✅      | Component | React testing library, Jest |
| App renders correctly                   | 🙅‍♂️      |           |                             |
| URL is correct                          | ✅      | Component | React testing library, Jest |
| App looks as expected on web and mobile | 🙅‍♂️      |           |                             |
| Front-end performance is at least a B   | 🙅‍♂️      |           |                             |
| App is secure                           | 🙅‍♂️      |           |                             |
| App is accessibility friendly           | 🙅‍♂️      |           |                             |

- Learn about [webdriverio](https://webdriver.io/docs/gettingstarted) and [screenerio](https://screener.io/)
- install wdio

```bash
npm install @wdio/cli
```

- setup wdio

`npx wdio config`

- paste the following code as the new test

```js
describe("My React application", () => {
  it("should look correct", () => {
    browser.url("");
    browser.execute("/*@visual.init*/", "My React App");
    browser.execute("/*@visual.snapshot*/", "Home Page");
    const result = browser.execute("/*@visual.end*/");
    expect(result.message).toBeNull();
  });
});
```

**🧪️Test Plan**

| Expected Behavior                       | Tested? | Test Type  | Technologies                |
| --------------------------------------- | ------- | ---------- | --------------------------- |
| A URL with the right text exists        | ✅      | Component  | React testing library, Jest |
| App renders correctly                   | ✅      | visual d2d | Webdriverio, Screener.io    |
| URL is correct                          | ✅      | Component  | React testing library, Jest |
| App looks as expected on web and mobile | ✅      | visual d2d | Webdriverio, Screener.io    |
| Front-end performance is at least a B   | 🙅‍♂️      |            |                             |
| App is secure                           | 🙅‍♂️      |            |                             |
| App is accessibility friendly           | 🙅‍♂️      |            |                             |

---

## Birthday Reminder React App

## Getting started

```js
cd birthday-reminder
npm i && npm start
//run tests
npm run wdio
```

[The production version of the website](https://laughing-feynman-11feb4.netlify.app/)

---

## Personal Portfolio

## Get started

```
npm i && npm run dev
```

## About repo

- Using NextJs
- React
- Styled components (each component has a corresponding ComponentStyles.js file)

## Testing

### visual testing

For visual testing I had to enable an [ignore threhold](https://docs.happo.io/docs/compare-threshold)

### functional testing

- how do we test the links in Projects.js?

### front-end perf

`cy.lighthouse(), Electron is not supported. Skipping...` error was a result of running Cypress on Electron. Changing to Chrome browser fixed the issue.

### updating npm packages

Use [npm-check](https://koalatea.io/how-to-update-all-your-npm-packages-at-once)

---

## Idea:

The idea is from [freecodecamp.com](https://koalatea.io/how-to-update-all-your-npm-packages-at-once)
