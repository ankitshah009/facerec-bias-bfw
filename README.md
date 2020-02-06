# Face Recognition: Too Bias, or Not Too Bias?


<div>
<blockquote>
         Joseph P. Robinson, Yann Henon, Gennady Livitz, Can Qin, Yun Fu, and Samson Timoner.
         <a href="papers/tpami-final.pdf"> Face Recognition: Too Bias, or Not Too Bias?</a> CoRR, abs/????.?????, 2020.
</blockquote>
</div>
<div>
    <div>
      <a href="papers/pami-appendix.pdf"> Appendix</a>  | 
      <a href="https://northeastern-my.sharepoint.com/:u:/g/personal/robinson_jo_northeastern_edu/EY2_oZ3xCspJrGLms8nOy-cBjKJO_Azd7XemctvusWp1vw?e=TLBmhm">Download Data</a> 
     </div>
    <div style="display: none;" id="robinsonfacebias2020">
      <pre class="bibtex">@article{robinson:facebias:2020,
      author        = "Joseph Robinson and Yann Henon and Gennady Livitz and Can Qin and Yun Fu and Samson Timoner",
      title         = "Face Recognition: Too Bias, or Not Too Bias?",
      journal       = "CoRR",
      year          = "2020",
      volume        = "abs/????.?????",
      url           = "http://arxiv.org/abs/????.?????",
      archiveprefix = "arXiv",
      eprint        = "????.?????",
      timestamp     = "Wed, 29 May 2019 11:27:50 +0200",
      biburl        = "https://dblp.org/rec/bib/journals/corr/abs-????-?????",
      bibsource     = "dblp computer science bibliography, https://dblp.org"
      }
    </pre>
  </div>

## Overview
Our findings reveal a bias in scoring sensitivity across different subgroups when verifying the identity of a subject
using facial images. In other words, the performance of a FR system on different subgroups (e.g., male vs female,
asian vs black) typically depends on a global threshold (i.e., decision boundary on scores or distances to determine
whether true or false pair). Our work uses fundamental signal detection theory to show that the use of a single,
global threshold causes a skew in performance ratings across different subgroups. For this, we demonstrate that
subgroup-specific thresholds are optimal in terms of overall performance and balance across subgroups.

Furthermore, we built and released the facial image dataset needed to address bias from this view of FR. Namely, *Bias Faces in the Wild* (BFW).

<img src="docs/bfw-teaser-image.png" alt="teaser" width="600"/>


Check out research paper, [https://github.com/visionjo/BFW-Face-Bias-Paper/blob/6900ea205381c4979e24e801cf670dfe314bf936/latest-version.pdf](https://github.com/visionjo/BFW-Face-Bias-Paper/blob/6900ea205381c4979e24e801cf670dfe314bf936/latest-version.pdf)

See [data/README.md](data/README.md) for more on BFW.

See [results/README.md](results/README.md) for more on results and experiments.

Register and download via this [form](https://forms.office.com/Pages/ResponsePage.aspx?id=gcLuqKOqrk2sm5o5i5IV57dX0R2T-YhEje_JmPbemGlUOTVZTkhPVElCSkRFMlZaOEVDSkJYWjk5Uy4u).

## Abstract

We reveal critical insights into problems of bias in state-of-the-art facial recognition (FR) systems using a novel 
Balanced Faces In the Wild (BFW) dataset: data balanced in gender and for ethnic groups. Classic signal detection theory 
was applied to understand the score distribution across different subgroups. Specifically, in face verification using 
Sphere-Face, we show that the optimal threshold varies across different subgroups of face-pairs. Thus, the conventional 
approach of learning a single, global threshold on all data yields a threshold biased to subgroups. We leveled out 
performances across different subgroups while improving the overall performance by learning a threshold per subgroup. 
Furthermore, we conduct a human evaluation to measure the bias in humans (i.e., within versus across subgroups), which 
supports the hypothesis that such a bias exists in human perception.

## Software implementation
All source code used to generate the results and figures in the paper are in
the `code` folder.
The calculations and figure generation are all run inside
[Jupyter notebooks](http://jupyter.org/).
The data used in this study is provided in `data` and the sources for the
manuscript text and figures are in `manuscript`.
Results generated by the code are saved in `results`.
See the `README.md` files in each directory for a full description.


## Getting the code

You can download a copy of all the files in this repository by cloning the
[git](https://git-scm.com/) repository:

    git clone https://github.com/visionjo/facerec-bias-bfw.git

or [download a zip archive](https://github.com/visionjo/facerec-bias-bfw/archive/master.zip).

A copy of the repository is also archived at *insert DOI here*


## Dependencies

You'll need a working Python environment to run the code.
The recommended way to set up your environment is through the
[Anaconda Python distribution](https://www.anaconda.com/download/) which
provides the `conda` package manager.
Anaconda can be installed in your user directory and does not interfere with
the system Python installation.
The required dependencies are specified in the file `environment.yml`.

We use `conda` virtual environments to manage the project dependencies in
isolation.
Thus, you can install our dependencies without causing conflicts with your
setup (even with different Python versions).

Run the following command in the repository folder (where `environment.yml`
is located) to create a separate environment and install all required
dependencies in it:

    conda env create


## Reproducing the results

Before running any code you must activate the conda environment:

    source activate ENVIRONMENT_NAME

or, if you're on Windows:

    activate ENVIRONMENT_NAME

This will enable the environment for your current terminal session.
Any subsequent commands will use software that is installed in the environment.

To build and test the software, produce all results and figures, and compile
the manuscript PDF, run this in the top level of the repository:

    make all

If all goes well, the manuscript PDF will be placed in `manuscript/output`.

You can also run individual steps in the process using the `Makefile`s from the
`code` and `manuscript` folders. See the respective `README.md` files for
instructions.

Another way of exploring the code results is to execute the Jupyter notebooks
individually.
To do this, you must first start the notebook server by going into the
repository top level and running:

    jupyter notebook

This will start the server and open your default web browser to the Jupyter
interface. In the page, go into the `code/notebooks` folder and select the
notebook that you wish to view/run.

The notebook is divided into cells (some have text while other have code).
Each cell can be executed using `Shift + Enter`.
Executing text cells does nothing and executing code cells runs the code
and produces it's output.
To execute the whole notebook, run all cells in order.

## To Do
- [x] Begin Template
- [x] Create demo notebooks
- [x] Add manuscript
- [ ] Documentation (sphinx)
- [ ] Update README (this)
- [ ] Complete test harness
- [ ] Modulate (refactor) code
- [ ] Add scripts and CLI

## License

All source code is made available under a BSD 3-clause license. You can freely
use and modify the code, without warranty, so long as you provide attribution
to the authors. See `LICENSE.md` ([LICENSE](LICENSE.md)) for the full license text.

The manuscript text is not open source. The authors reserve the rights to the
article content, which is currently submitted for publication in the
2020 IEEE Conference on AMFG.

## Acknowledgement
We would like to thank the [PINGA](https://github.com/pinga-lab?type=source) organization on Github for the
 [project template](https://github.com/pinga-lab/paper-template) used to structure this project.
