# Storybook : 

- An interactive **directory** of your UI components and their stories.
- Storybook is packaged as a small, development-only, workshop that lives alongside your app.
- It helps you focus development on each variation of a component, even the hard-to-reach edge cases.
- Jump straight to working on a UI component in a specific state.
- Build and test individual components outside of the main development environment of the project.
- Can quickly create real product scenarios without having to build that functionality out for real.
  - *Like What does the dashboard look like if the user is brand new vs a veteran user? What does the logged in header look like vs logged out header?*
- Showcases components interactively in an isolated development environment

## Stories ?

> Capture UI variations as “stories”

- When developing a component variation in isolation, save it as a story. 
- 'Stories are a declarative syntax for *supplying props and mock data* to simulate component variations. 
- Each component can have *multiple stories*. 
- Each story allows you to demonstrate a *specific variation* of that component to verify appearance and behavior.
- You write stories for granular UI component variation and then use those stories in development, testing, and documentation.
- Storybook is the single source of truth for your UI. 
- Stories index all your components and their various states, making it easy for your team to find and reuse existing UI patterns. 
- Storybook also auto-generates *documentation* from those stories.
- Each story is exported as a JavaScript function enabling you to reuse it with other tools. 

# Project steps :

1. Setup 
```bash
npx storybook@latest init
```
Based on project's dependencies, storybook will provide you the setup with the best configuration available. 
2. `.storybook\` folder contains configurations.
   1. `main.js` describes to export the stories files and addons. Can say that this file is a cofiguration for storybook.
   2. `preview.js` contains configurations for stories. Can say that this file is a cofiguration for stories....
3. Was getting error with `npm run storybook` :
```error
C:\Users\meet.makwana\Desktop\Learnings\react-storybook-v6\node_modules\@storybook\cli\bin\index.js:23
  throw error;
  ^

Error: Cannot find module 'C:\Users\meet.makwana\Desktop\Learnings\react-storybook-v6\node_modules\pathe\dist\index.cjs'
    at createEsmNotFoundErr (node:internal/modules/cjs/loader:960:15)
    at finalizeEsmResolution (node:internal/modules/cjs/loader:953:15)
    at resolveExports (node:internal/modules/cjs/loader:482:14)
    at Function.Module._findPath (node:internal/modules/cjs/loader:522:31)
    at Function.Module._resolveFilename (node:internal/modules/cjs/loader:919:27)
    at Function.Module._load (node:internal/modules/cjs/loader:778:27)
    at Module.require (node:internal/modules/cjs/loader:1005:19)
    at require (node:internal/modules/cjs/helpers:94:18)
    at Object.<anonymous> (C:\Users\meet.makwana\Desktop\Learnings\react-storybook-v6\node_modules\giget\dist\index.cjs:6:15)
    at Module._compile (node:internal/modules/cjs/loader:1101:14) {
  code: 'MODULE_NOT_FOUND',
  path: 'C:\\Users\\meet.makwana\\Desktop\\Learnings\\react-storybook-v6\\node_modules\\pathe\\package.json'
}
```

and inpected and corrected the filename of index file of that dependency in the node_modules\pathe\dist\index.cjs
- Issues were very persistent with the create-react-app so sticked with vitejs(js+swc).
  
4. he