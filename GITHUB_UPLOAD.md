# GitHub Upload Guide

This folder is prepared as a clean GitHub repository upload.

## Recommended repository
- Repository name: `chubb-apac-qa-assessment`
- Visibility: **Public** if the client must open it without signing in.

## Upload with Git

```bash
git init
git branch -M main
git add .
git commit -m "docs: submit Chubb APAC QA assessment"
git remote add origin https://github.com/YOUR-USERNAME/chubb-apac-qa-assessment.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username.

## Final client link

After pushing, share:

`https://github.com/YOUR-USERNAME/chubb-apac-qa-assessment`

Anyone can view the repository when its visibility is **Public**.

## Important

Do not commit `.env` files containing real credentials, API keys, tokens, or passwords. The repository includes `.env.example` for configuration reference.
