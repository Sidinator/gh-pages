### install gh-pages package

1. run `npm install gh-pages --save-dev`
2. Edit the package.json to include `"predeploy": "npm run build",`
`"deploy": "gh-pages -d dist",` This should be added after `"build": "vite build`. File to look like
<details><summary>code</summary>

```javascript
"scripts": {
"dev": "vite",
"predeploy": "npm run build",
"deploy": "gh-pages -d dist",
"build": "vite build",
"lint": "eslint src --ext js,jsx --report-unused-disable-directives --max-warnings 0",
"preview": "vite preview"
```

3. edit the vite.config.js with `base: "/repo name",` Add this on the line befor `plugins: [react()],`
</details>

[Setup guide](https://dev.to/rashidshamloo/deploying-vite-react-app-to-github-pages-35hf)
