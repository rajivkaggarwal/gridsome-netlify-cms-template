# Default starter for Gridsome + Netlify + Netlify CMS

Started by running `gridsome create gridsome-netlify-cms-template`.

Then used the instructions from here: https://gridsome.org/docs/guide-netlify-cms/

### 1. To run locally

`gridsome develop`

### 2. Adapting to yourself

1. Fork this repo
2. `cd` into this directory
3. `npm install` to install npm modules
4. In `src/admin/config.yml` you'll need to change the `name` and `repo` under `backend` for your repo
5. Follow this instructions to enable Netlify CMS authentication via GitHub: https://gridsome.org/docs/guide-netlify-cms/#netlify-cms-authentication-with-github

### 3. Deployment with Netlify

1. Sign up for Netlify: netlify.com
2. Add a new site<br/>
![New Site from Git](readme_content/new_site.png)
3. Use GitHub<br/>
![Choose GitHub](readme_content/choose_github.png)
4. Specify `npm run build` and `dist`<br/>
![Choose GitHub](readme_content/specify_build_dist.png)