|                                          **Rapid Access**                                                 |
|:--------------------------------------------------------------------------------------------------------- |
| [![Dev](https://img.shields.io/badge/docs-dev-blue.svg)](https://JuliusTechCo.github.io/JuliusGraph/dev/) |

# Welcome to Graph Computing! 👋

We are a group of researchers and engineers passionate about graph computing. We believe
graph technology is the future for solving the most challenging problems in computing. We 
spent the past few years at [Julius Technologies](https://www.juliustech.co/) building 
a truly innovative graph computing solution, the Julius Graph Engine. 

In this repository, you will find a number of tutorials that explain the awesomeness of 
graph computing. These tutorials show how to use graph computing to build real solutions for 
real world problems, they will help you to quickly get started with graph programming and 
graph computing. We promise that you will feel enlighted by graph computing once you 
go through these tutorials. You will never look at programming the same way again!

To report issues, request new features or general inquiries, please raise a github issue 
in this repo, or email us at info@juliustech.co.

## Tutorials

Our tutorials are available in two formats:

- As interactive jupyter notebooks hosted on a jupyterhub server. It is the best format for 
you to learn and experiment with Julius Graph Engine. To gain access to these online tutorial 
notebooks, you need to follow the instructions below to [register for developer
  access](https://github.com/JuliusTechCo/JuliusGraph#register-for-developer-access), it only
  takes a minute to register and it is free!

- As static HTML pages, which show the entire source code and results, but they are 
not interactive. If you want to read about Julius Graph Engine and its capabilities 
without register for developer access, please click [here](https://JuliusTechCo.github.io/JuliusGraph/dev/) 
to read the tutorials in HTML format. The HTML is also a good format to share with 
your colleagues or fellow developers.

### Register for Developer Access

Requesting developer access is super easy and should not take more than a minute. Please,
proceed to this [link](https://backendgraph.com/user/signup). The web site use Google authentication, 
if you are already logged in with your Google account, you will be prompted with some auto-populated 
fields:

<p align="center">
  <img width=50% src="assets/signup_1.png">
</p>

Complete the missing information and hit *Request access*. You can also change your current
account if wanted. On the other hand, you will be asked to log into your Google account if
you are not currently logged in:

<p align="center">
  <img width=50% src="assets/signup_2.png">
</p>

Once you registered and agreed the term of service, you will be prompted to the following page:

<p align="center">
  <img width=50% src="assets/landingpage.png">
</p>

That's it! You have registered as a Julius developer and you are now able to proceed to our
Jupyter Lab Environment by clicking *Go to Lab Environment*. That was easy!

The following step is required only once and will ask you to Sign In to our Jupyter Hub
server:

<p align="center">
  <img width=50% src="assets/jupyter_signin.png">
</p>

Clicking *Sign in with Google* will land in a standard Jupyter Hub/Juypter Lab session:

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
concepts explained in previous ones. However, we have you covered even if you are short on
time!. In that case, we recommend reading (at least):
* [Quick Start](https://JuliusTechCo.github.io/JuliusGraph/dev/pages/t001_quickstart.html),
* [MapReduce](https://JuliusTechCo.github.io/JuliusGraph/dev/pages/t003_mapreduce.html) and
* [Distributed Machine Learning Pipeline](https://JuliusTechCo.github.io/JuliusGraph/dev/pages/t004_bagging.html).

Those tutorials should give you some good ideas on the power of graph computing on 
Julius' Graph Engine.

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
