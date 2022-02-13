# GitHub Stats Visualizations : Transparent
> Generate visualizations of GitHub user and repository statistics using GitHub
Actions.

<a href="https://github.com/rahul-jha98/github-stats-transparent">

![](https://raw.githubusercontent.com/dkssud8150/github-stats-transparent/output/generated/overview.svg)
![](https://raw.githubusercontent.com/dkssud8150/github-stats-transparent/output/generated/languages.svg)

</a>

> NOTE: This repository is my extension of the repo [jstrieb/github-stats](https://github.com/jstrieb/github-stats). This repo was meant to serve as a detached fork of his project. If you like this repository make sure you also star his repository to show appreciation for his work. 

## ⚠️ Disclaimer

The project uses access token that has read access to private repositories and if there is any
exception while reading data from any repository it throws Exception which is printed in the workflow logs. 
This exception will be viewable in the Actions tab of the repository fork, and
anyone may be able to see the name of one or more private repositories.

## ⚙️ Installation

<!-- TODO: Add details and screenshots -->

1. Create a personal access token (not the default GitHub Actions token) using
   the instructions
   [here](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).
   Personal access token must have permissions: `read:user` and `repo`. Copy
   the access token when it is generated – if you lose it, you will have to
   regenerate the token.

2. Click [here](https://github.com/rahul-jha98/github-stats-transparent/fork) to create a
   fork of this repository

3. If this is the README of your fork, click [this
   link](../../settings/secrets/actions) to go to the "Secrets" page.
   Otherwise, go to the "Settings" tab of the newly-created repository and go
   to the "Secrets" page (bottom left).
   
   ![](https://raw.githubusercontent.com/rahul-jha98/github-stats-transparent/main/readme_images/Actions.png)
   
4. Create a new secret with the name `ACCESS_TOKEN` and paste the copied
   personal access token as the value.

   <img src='https://raw.githubusercontent.com/rahul-jha98/github-stats-transparent/main/readme_images/Token.png' height='250px'/>

5. If you want to ignore certain repos, add them (separated by commas) to a new
   secret—created as before—called `EXCLUDED`. 

   <img src='https://raw.githubusercontent.com/rahul-jha98/github-stats-transparent/main/readme_images/Exclude.png' height='250px'/>

6. If you want to ignore certain languages, add them (separated by commas) to a new secret called 
   `EXCLUDED_LANGS`.

7. By default the languages, stars, forks and repository views do not consider stats from 
   public repositories that you have forked and contributed to. But if you want to count stats from
   forked repositories also you can do so by creating a new secret called `COUNT_STATS_FROM_FORKS`. 
   For the value you can put any random value because the action only checks if the secret is set or not.

   <img src='https://raw.githubusercontent.com/rahul-jha98/github-stats-transparent/main/readme_images/Forks.png' height='250px'/>

8. Go to the [Actions Page](../../actions?query=workflow%3A"Generate+Stats+Images") and press "Run
   Workflow" on the right side of the screen to generate images for the first
   time. The images will be periodically generated every hour, but they can be
   manually regenerated by manually running the workflow.

9. Check out the images that have been created in the [`generated`](../output/generated)
   folder in `output` branch.

10. Link back to this repository so that others can generate their own
   statistics images.

11. Star this repo if you like it!


<br>
<br>

## 🤔 Why Transparent ??
With the introduction of dark mode in Github it has become difficult to set an image background that looks consistent with the background in both dark and light mode. 

To solve this the most obvious solution was to make the background transparent. All that was left was to choose colors for text that makes it legible in light as well as dark background.

After wasting a day playing with different color values finally settled on one. Hope you like it. 

![](https://raw.githubusercontent.com/rahul-jha98/github-stats-transparent/main/readme_images/light.png)

![](https://raw.githubusercontent.com/rahul-jha98/github-stats-transparent/main/readme_images/dark.png)


## Related Projects

- Extension of a detached fork of [jstrieb/github-stats](https://github.com/jstrieb/github-stats)
- Inspired by a desire to improve upon
  [anuraghazra/github-readme-stats](https://github.com/anuraghazra/github-readme-stats)
- Makes use of [GitHub Octicons](https://primer.style/octicons/) to precisely
  match the GitHub UI
