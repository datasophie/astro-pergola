# Deploy an Astro site on Pergola

[Pergola](https://docs.pergola.cloud/docs/overview) is a deployment and runtime platform for web and server applications, a high-availability cluster with auto-scaling, failover handling, fully managed TLS certificates and much more.

[Astro](https://astro.build/) is an all-in-one web framework for building content-driven websites like blogs, marketing, e-commerce, and more.

You can deploy your Astro site on Pergola in a matter of minutes, just follow the steps below.

## Deployment Steps

You need a Git repository with your Astro code and:

* If you do not have a `Dockerfile` in your repo yet, you can copy [from here](Dockerfile) and adapt as needed
* Add a `pergola.yaml` to your repo's root directory, the Project Manifest that describes your app, which you can also copy [from here](pergola.yaml)

👍 Your app is prepared. Now head over to [Pergola](https://console.pergola.cloud/) and deploy:

* Create a [new Project](https://console.pergola.cloud/pipeline/projects) and provide your Git repository's clone URL
  > you can also use this repo for testing
* Start a new Build
  > this will scan all branches for a valid `pergola.yaml`
* Create a new Stage of type `dev`
  > this will be the runtime environment for your Astro site
* Once the Build finishes successfully, navigate to the Stage created above
* Now hit `NEW RELEASE` and select the Build just finished
* ... and `DEPLOY`

🚀 **That's it! Your Astro site is live at the URL Pergola has provided.**

Here is a live example:
https://demo-astro-dev.apps.pergola.cloud/

## Further read

Want to learn more about [Projects](https://docs.pergola.cloud/docs/reference/projects), [Stages](https://docs.pergola.cloud/docs/reference/stages), [Releases](https://docs.pergola.cloud/docs/reference/releases)...?
Here is the full Pergola [documentation](https://docs.pergola.cloud).

## Contributing

Pull requests are always welcome! Thank you.
