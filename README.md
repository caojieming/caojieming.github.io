# James Cao's Personal Website

To preview website before deploy, use `hugo server` (server link: [http://localhost:1313/](http://localhost:1313/))

Update hugo using `npx hugoblox@latest upgrade`
- [Update documentation](https://docs.hugoblox.com/guides/upgrade/)

## Notes
- `/config/_default/params.yaml`: edit general website data
  - overall website name, light/dark mode, fonts, header/footer settings, copyright, SEO, locale, etc.
- `/content/_index.md`: edit the header contents/nav links
- `/content/_index.md`: edit the contents/layout of the landing page
- `/content/authors/admin`: edit information directly tied to an "author"
  - changing things here will affect the top half of the landing page details as well as the experience page
- `/static/uploads`: resume pdf location
- `/content/*/_index.md`: edit the contents/layout of the corresponding `*` page
- `/content/experience.md`: edit the contents/layout of the experience page

- if the branch name is `main`, then the website should deploy automtically (see file `/.github/workflows/deploy.yaml`)
  - you can change the auto-deploy branch-name trigger in said file
  - otherwise, go to Github -> Actions -> Deploy Website to GitHub Pages -> run workflow

## Troubleshooting
- if attempting to deploy to gh-pages results in failure, check details of workflow
  - if you get something like "Branch BRANCH_NAME is not allowed to deploy to github-pages due to environment protection rules", go to Settings -> Environments -> github-pages -> Deployment branches and tags -> add or edit BRANCH_NAME to the list

## Template used
[Hugo Academic CV Theme](https://github.com/HugoBlox/theme-academic-cv)
