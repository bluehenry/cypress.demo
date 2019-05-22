# cypress.demo
Cypress is a JavaScript open source testing framework, which provide fast and reliable testing for web apps, compared with Selenium/WebDriver.

Cypress.io is a relatively new framework designed to overcome many shortcomings found in Selenium, Phantom.js, and others before them. It uses an event-based architecture that hooks into Google Chrome’s lifecycle events, enabling it to wait for things like Ajax requests to complete without using a polling/timeout mechanism. This leads to reliable and fast tests.

Selenium and similar tools were designed to test applications that require a full-page refresh—supporting Ajax data fetching was an afterthought. This lead to many issues with timing and flakey tests: tests would sometimes fail due to slow API requests or network latency. Fixing these flakey tests typically required adding sleep statements and increasing timeouts, which made the test code more brittle. Not to mention extremely slow.

# Features
* Supports headless browser.
* Easy to integrate into CI/CD pipeline. 
* Visual testing with cypress-image-snapshot.

# Visual automation testing
```
cypress run --env failOnSnapshotDiff=false
cypress run --env failOnSnapshotDiff=false updateSnapshots=true
cy.setResolution([2560, 1440]);
```

## Taking a screenshot
Generating screenshots(.png files) in 'screenshots' folder.
```
cy.screenshot('dashboard');
```

## Matching a screenshot
cy.matchImageSnapshot() generates screenshots (.snap.png files) in 'snapthos/spec.js_file_path/' folders in the first run. Then it compares screensthos in the second run.
```
cy.matchImageSnapshot('dashboard');
```
