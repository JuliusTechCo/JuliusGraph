|                                          **Rapid Access**                                                 |
|:--------------------------------------------------------------------------------------------------------- |
| [![Dev](https://img.shields.io/badge/docs-dev-blue.svg)](https://JuliusTechCo.github.io/JuliusGraph/dev/) |

# Hey, Welcome 👋

In this repository you will find guidelines to access [Julius
Technologies](https://www.juliustech.co/) tutorials to learn and test our low-code graph
computing platform.

We are a group of researchers and engineers passionate about graph computing. We believe
this technology can tackle the most computational challenging problems out there. We are
Julius Technologies.

For any additional queries or suggestions do not hesitate to email us at info@juliustech.co.

## Tutorials

Our tutorials are available in two formats:

- As jupyter notebooks running on a server machine allowing an interactive learning
  experience. Please, refer to the [Request Developer
  Access](https://github.com/JuliusTechCo/JuliusGraph#request-developer-access) section for
  further details.

- As HTML pages, allowing a rapid access into the material without the need of any setup.
  Click [here](https://JuliusTechCo.github.io/JuliusGraph/dev/) to access the pre-compiled
  learning material. Keep in mind that setting up a developer environment in the following
  section is a really simple task and provides many more features.

### Request Developer Access

Requesting developer access is super easy and should not take more than a minute. Please,
proceed to [this](https://backendgraph.com/user/signup) link. If you are already logged in
with your Google account, you will be prompted with some auto-populated fields:

![Sign up with auto-populated fields.](assets/signup_1.png)

Complete the missing information and hit *Request access*. You can also change your current
account if wanted. On the other hand, you will be asked to log into your Google account if
you are not currently logged in:

![Sign up before logged in to Google.](assets/signup_2.png)

Once you requested access, you will be prompted to the following page:

![Welcome page with proceed to Lab.](assets/landingpage.png)

That's it! You have registered as a Julius developer and you are now able to proceed to our
Lab Environment by clicking *Go to Lab Environment*. That was easy!

The following step is required only once and will ask you to Sign In to our Jupyter Hub
server:

![Sign In to jupyter hub.](assets/jupyter_signin.png)

Clicking *Sign in with Google* will land in a well-known Jupyter Hub session:

![Jupyter Hub landing page.](assets/jupyter_landing.png)

Once you have completed all previous steps, you can come back at any time using the lab
route (try [this](https://backendgraph.com/lab) link).

### General Details

In your Jupyter Hub session you should see a couple of folders and a `README.md` file at the
left panel. Proceed to the `README.md` to checkout some useful suggestions.

On the other hand, each folder description proceeds:

* `assets`: holds images for tutorials,
* `data`:  holds data files for tutorials,
* `tutorials`: holds tutorials as jupyter notebooks,
* `persist`: you should locate your work and progress here to make sure it won't be lost if
  the server is restarted.

Ideally, tutorials should be read in order. This is because some tutorials depend on
concepts explained in previous ones. However, we have you covered even if you are short in
time!. In that case, we recommend reading (at least):
* [Quick Start](https://JuliusTechCo.github.io/JuliusGraph/dev/pages/t001_quickstart.html),
* [MapReduce](https://JuliusTechCo.github.io/JuliusGraph/dev/pages/t003_mapreduce.html) and
* [Distributed Machine Learning Pipeline](https://JuliusTechCo.github.io/JuliusGraph/dev/pages/t004_bagging.html).

Those tutorials should be enough to checkout some powerful features.

### Running a Tutorial

All tutorials come with a short paragraph explaining how to run them. We reference those
suggestions below for completeness purposes:

* Select "run all cells" on this notebook from the Run menu in Jupyter notebook or Jupyter
  lab. This step will produce intermediate data output and charts.
* Some cells print out a url, which you can click on and bring up an interactive web UI to
  visualize the graph data.
* In the unlikely event that the notebook becomes irresponsive, you can try "Restart
  Kernel" from the Kernel menu, then run individual cells one by one using `Shift+Enter`.
* Some tutorials use local clusters consisting of multiple processes to mimic the effects
  of graph distribution over a remote clusters. By default, these local clusters
  automatically stop after idling for 15 minutes to conserve CPU and memory resources. You
  will need to rerun the entire notebook if your local cluster stopped due to inactivity.
* Additional resources (video demos & blogs) are available in our
  [website](http://juliustech.co).
* To report any issues, get help or request features, please raise an issue
  [here](https://github.com/JuliusTechCo/JuliusGraph/issues).

### Web User Interface

Each time a tutorial displays a graph, you will be prompted with an url as well that
redirects to the Julius WebUI. This great tool is a work in progress with many features
already included, so enjoy it! The following are some snapshots for your reference:

![WebUI for a non distributed computation case.](assets/webui_1.png)

![WebUI for a distributed computation case.](assets/webui_2.png)

Thank you for reading up to this point 🙌. If you are interested in our technology, don't
hesitate to get in touch. We would love building incredible solutions with you for real life
problems.
