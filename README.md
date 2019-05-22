# cypress.demo
Cypress is a JavaScript open source testing framework, which provide fast and reliable testing for web apps, compared with Selenium/WebDriver.
Cypress supports headless browser, easy to integrate into CI/CD pipeline.
Visual testing with cypress-image-snapshot.

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
