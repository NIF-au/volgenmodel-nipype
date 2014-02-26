# volgenmodel-nipype

Port of volgenmodel to Nipype along with interfaces for a number of Minc tools.

# Install

Prerequisites:

* https://github.com/nipy/nipype
* https://github.com/BIC-MNI/minc-widgets
* bestlinreg
* minccomplete

Then:

    git clone https://github.com/carlohamalainen/volgenmodel-nipype
    cd volgenmodel-nipype
    export PYTHONPATH=`pwd`

Load the ```volgenmodel.py``` script using IPython or similar, being sure to
tweak ```FAST_EXAMPLE_BASE_DIR``` to something appropriate. Then

    workflow.run()

runs the workflow on a single core, or

    workflow.run(plugin='MultiProc', plugin_args={'n_procs' : 4})

runs it on 4 cores.

The workflow for a small 3-stage model is:

![workflow fast-example](https://github.com/carlohamalainen/volgenmodel-nipype/raw/master/volgenmodel_graph.png)
