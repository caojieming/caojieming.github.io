# James Cao's Personal Website

## Dev tools
Standard npm updating:<br>
`npm install` to install all dev dependencies.<br>
`npm outdated` to check if any packages are outdated (optional).<br>
`npm update` to update outdated packages.<br><br>

How to update:
- ~~Update hugo using `hbx upgrade`~~
- ~~[Update documentation](https://docs.hugoblox.com/guides/upgrade/)~~
- Above is deprecated, "upgrade.yml" Workflow should automatically update hugoblox every monday

If you're getting build errors after hugoblox updates try updating the following files from the [original hugo repo](https://github.com/HugoBlox/hugo-theme-academic-cv):
- ~/hugoblox.yaml from [hugo repo](https://github.com/HugoBlox/hugo-theme-academic-cv/blob/main/hugoblox.yaml)
- ~/.github/workflows/build.yml from [hugo repo](https://github.com/HugoBlox/hugo-theme-academic-cv/blob/main/.github/workflows/build.yml) into your own.
- ~/go.mod from [hugo repo](https://github.com/HugoBlox/hugo-theme-academic-cv/blob/main/go.mod)
- ~/config/_default/hugo.yaml from [hugo repo](https://github.com/HugoBlox/hugo-theme-academic-cv/blob/main/config/_default/hugo.yaml)
- ~/config/_default/module.yaml from [hugo repo](https://github.com/HugoBlox/hugo-theme-academic-cv/blob/main/config/_default/module.yaml)
<br><br>

To preview website before deploy, use `hugo server` (server link: [http://localhost:1313/](http://localhost:1313/))

## Notes
- `/config/_default/params.yaml`: edit general website data
  - overall website name, light/dark mode, fonts, header/footer settings, copyright, SEO, locale, etc.
- `/config/_default/menus.yaml`: edit the header contents/nav links
- `/content/_index.md`: edit the contents/layout of the landing page
  - resume link is here
- `/static/uploads`: resume pdf location
- `/content/*/_index.md`: edit the contents/layout of the corresponding `*` page
- `/content/experience.md`: edit the contents/layout of the experience page

- `/data/authors/me.yaml`: edit information directly tied to an "author"
  - changing things here will affect the top half of the landing page details as well as the experience page
- `/assets/media/authors/me.png`: edit author picture

- if the branch name is `main`, then the website should deploy automtically (see file `/.github/workflows/deploy.yaml`)
  - you can change the auto-deploy branch-name trigger in said file
  - otherwise, go to Github -> Actions -> Deploy Website to GitHub Pages -> run workflow

## Troubleshooting
- if attempting to deploy to gh-pages results in failure, check details of workflow
  - if you get something like "Branch BRANCH_NAME is not allowed to deploy to github-pages due to environment protection rules", go to Settings -> Environments -> github-pages -> Deployment branches and tags -> add or edit BRANCH_NAME to the list

## Template used
[Hugo Academic CV Theme](https://github.com/HugoBlox/theme-academic-cv)
