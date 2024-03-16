- <h1>👋 Hi, I’m Vijay Bochare</h1>
- 👀 I’m Software Engineer  
- 🌱 I’m currently learning Nextjs.
- 💞️ I’m looking to collaborate on ...
- 📫 Passionate about Coding and learning New technology.
- 😄 Pronouns: he/him...


<!---
Vijay4649/Vijay4649 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<div id="header" align="center">
  <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" width="100"/>
</div>

<br>

![](https://visitor-badge.laobi.icu/badge?page_id=Vijay4649.Vijay4649)
[![Github](https://img.shields.io/github/followers/Vijay4649?label=Follow&style=social)](https://github.com/Vijay4649)

## 🧰 Languages and Tools:
<p align="center">
<img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/python/python.png" alt="Python" height="40" style="vertical-align:top; margin:4px">
<img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/javascript/javascript.png" alt="Javascript" height="40" style="vertical-align:top; margin:4px">
<img src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/visual-studio-code/visual-studio-code.png" alt="VS Code" height="40" style="vertical-align:top; margin:4px">
</p>

# Blog posts
<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->


name: Latest blog post workflow
on:
  schedule: # Run workflow automatically
    - cron: '0 * * * *' # Runs every hour, on the hour
  workflow_dispatch: # Run workflow manually (without waiting for the cron to be called), through the GitHub Actions Workflow page directly
permissions:
  contents: write # To write the generated contents to the readme

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Pull in dev.to posts
        uses: gautamkrishnar/blog-post-workflow@v1
        with:
          feed_list: "https://dev.to/feed/gautamkrishnar,https://www.gautamkrishnar.com/feed/"
