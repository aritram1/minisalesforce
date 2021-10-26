# MiniSalesforce

Experience salesforce in a mini app.

Frontend..

1. Create standard lwc app
    - `npx create-lwc-app minisalesforce`
2. Prerequisites for using slds and base components to our project.
    - install npm packages for lwc base components and slds
        `npm install lightning-base-components`
        `npm install @salesforce-ux/design-system --save-dev`
    - Add following line in `modules` key in lwc.config.json to ensure the base-components dependency is specified
        `{ "npm": "lightning-base-components" }`
    - Add following line  to `resources` list in lwc-services.config.js to configure SLDS
        `{ from: 'node_modules/@salesforce-ux/design-system/assets', to: 'src/SLDS' },{ from: 'node_modules/@salesforce-ux/design-system/assets', to: 'dist/SLDS' }`
    - Add following as the `first line` in index.js to activate synthetic shadow
        `import @lwc/synthetic-shadow`
    - Add following line to index.html to include slds in our app
        `<link rel="stylesheet" href="/SLDS/styles/salesforce-lightning-design-system.min.css"/>`
2. create a home app inside /src
3. Show login related values in a record view form
4. On clicking the Login the Auth will start.

Over to backend...
