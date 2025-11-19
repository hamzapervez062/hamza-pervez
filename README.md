# Hamza — Portfolio

This repository contains a simple static portfolio site.

How to publish to GitHub Pages (quick steps):

- Create a GitHub repository and push these files to the `main` branch.
- The included GitHub Actions workflow will deploy the repository root to the `gh-pages` branch automatically on each push to `main`.
- The `CNAME` file (present in this repo) will configure a custom domain if DNS is pointed correctly.

PowerShell commands (run from the `hamza` folder):

```powershell
git init
git add .
git commit -m "Initial commit"
# create repo on GitHub and add remote, or use `gh repo create` (see below)
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

Optional: create repo and push using GitHub CLI:

```powershell
gh repo create <your-username>/<your-repo> --public --source=. --remote=origin --push
```

DNS notes for `CNAME`:
- For apex domains (example.com) add A records pointing to: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
- For subdomains (www.example.com) add a CNAME record pointing to `<your-username>.github.io`.

If you want, I can run the local git commands and help create the GitHub repo (if you allow and have `gh` configured).