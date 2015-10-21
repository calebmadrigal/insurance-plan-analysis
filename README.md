# insurance-plan-analysis

IPython Notebook (Project Jupyter) notebooks I put together to analyze my personal insurance options at job. Though not very nicely documented, you may find them useful to analyze your insurance plans as well.

### View Read-only Online:

* [FireEye 2015 Family Plan](http://nbviewer.ipython.org/github/calebmadrigal/insurance-plan-analysis/blob/master/fireeye-insurance-family-2015.ipynb)
* [FireEye 2015 Individual Plan](http://nbviewer.ipython.org/github/calebmadrigal/insurance-plan-analysis/blob/master/fireeye-insurance-individual-2015.ipynb)
* [Wipfli 2014 Family Plan](http://nbviewer.ipython.org/github/calebmadrigal/insurance-plan-analysis/blob/master/WipfliHealthInsurance2014.ipynb)


### How to run

There are two options to run these...

#### Option 1: IPython Notebook installed with dependencies

Install IPython Notebook (Project Jupyter) along with dependencies (TBD), and then you can run:

    ipython3 notebook


#### Option 2: Data Science Toolkit

I recommend running these with the [Data Science Toolkit](http://datasciencetoolbox.org/) Vagrant box, which comes with IPython Notebook and the scientific computing stack.

Here are the directions to get the Data Science Toolkit setup:

(Get Vagrant and VirtualBox)

Run Vagrant:

    vagrant init data-science-toolbox/dst
    vagrant up
    vagrant ssh

Setup IPython Notebook

    dst setup base

Add line to Vagrantfile:

    cd /vagrant
    nano Vagrantfile
    config.vm.network "forwarded_port", guest: 8888, host: 8888

Exit vagrant ssh and run:

    vagrant reload
    vagrant ssh
    cd /vagrant

Change these to lines to below in ~/.ipython/profile_dst/ipython_notebook_config.py:

    c.FileNotebookManager.notebook_dir = u'/vagrant'
    c.NotebookManager.notebook_dir = u'/vagrant'

Run IPython Notebook:

    sudo ipython notebook --profile=dst

On host machine, go to this URL:

    https://localhost:8888

