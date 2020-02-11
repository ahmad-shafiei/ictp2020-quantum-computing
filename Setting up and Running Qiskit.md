Setting up Qiskit
=================

Open a Terminal window so that you can copy and paste the commands
listed below. You can mark whole lines by triple-clicking on them. To
copy, use Ctrl+C, to paste into the Terminal window, use Ctrl+Shift+V.

1.  Activate our Anaconda 3 installation by placing an empty file named
    `.use_ictp_anaconda3` in your home directory:\

        touch .use_ictp_anaconda3

2.  Log out and log in again so that the change takes effect.
3.  Create an Anaconda directory on the local hard disk in order to
    reduce the work load on the file servers:\

        mkdir /scratch/$USER/.anaconda3
        ln -s /scratch/$USER/.anaconda3 $HOME

    Note that by doing this you will always have to return to the same
    desktop computer, so remember its name/position.

4.  Prepare your Linux shell for use with Anaconda:\

        conda init bash

5.  Create a conda environment and activate it:\

        conda create -n qiskit-env python=3
        conda activate qiskit-env

6.  Install the Qiskit library:\

        pip install qiskit

7.  For Jupyter, we have to create a corresponding environment:\

        pip install ipykernel
        python -m ipykernel install --user --name=qiskit-env

8.  Download the notebook we are going to use:
    [teleportation\_superdensecoding\_solutions\_mys.ipynb](https://users.ictp.it/~johannes/qiskit/teleportation_superdensecoding_solutions_mys.ipynb)\
     Choose the **Save** option, don't open the file using an
    application (e.g. RStudio).

Running Qiskit
==============

Once this is done, you can start up a Jupyter notebook using the
command\

    jupyter-notebook

Navigate to your download folder, and click on the downloaded file.
Before running it, go to the **Kernel** menu and **Change Kernel** to
**qiskit-env**.


