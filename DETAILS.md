# Details

This repository is for demonstration purposes for how to deploy a Astro application on Pergola. It contains a vanilla Astro site, with no extras and especially no dependencies to or adjustments made for Pergola.

It is fully prepared and ready to be deployed. If you do not have your own Astro Git repository yet, feel free to deploy this one on Pergola for testing.

Here you can see a [Astro deployment on Pergola](https://console.pergola.cloud/pipeline/projects/astro/stages/dev) in action.

## Ingredients

The [Dockerfile](Dockerfile) compiles your Astro app into a portable container image, production ready and served by Nginx.

The [nginx/](nginx/) folder contains a few useful tweaks, inspired by this [how-to recipe](https://docs.astro.build/en/recipes/docker/#nginx).

The [pergola.yaml](pergola.yaml), aka the [Project Manifest](https://docs.pergola.cloud/docs/reference/project-manifest), is the main and the only file specific to Pergola in order to build, deploy and run your Astro site.

The Astro site has been created with this command:

```bash
npm create astro@latest -- site --install --template blog
```

Thus, the Astro code is available under [site/](site/), makes it easier to manage. But ofc, this is a matter of taste. If you prefer, you can keep it at top level in your repository.
