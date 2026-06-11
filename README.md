# WDF World Cup Prediction Dashboard

Clean rebuilt package for GitHub Pages.

Your repository must contain exactly these items at the root:

- index.html
- .nojekyll
- results.json
- README.md
- .github/workflows/update-results.yml

Important: index.html is the dashboard. update-results.yml must only be inside .github/workflows/.

After upload:
1. Settings -> Pages -> Deploy from branch -> main -> / (root)
2. Settings -> Actions -> General -> Workflow permissions -> Read and write permissions
3. Actions -> Update World Cup results -> Run workflow
