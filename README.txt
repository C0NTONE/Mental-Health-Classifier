README
INSTRUCTIONS FOR CREATING AND ACCESSING CONDA ENVIRONMENT ON CLUSTER
1. FROM SHELL, ENTER conda create -n mentalhealth pytorch huggingface_hub transformers IN COMMAND PROMPT
                                    ^NAME OF ENV^  ^LIBRARIES REQUESTED TO BE IN ENV^
2. ENTER y WHEN PROMPTED (y/n)?
3. ACTIVATE THE CONDA ENVIRONMENT USING conda activate mentalhealth
4. INSTALL THE KERNEL USING conda install ipykernel
5. CHOOSE y IF PROMPTED (y/n)?
6. TO CREATE AN ACCESSIBLE KERNEL FROM JUPYTER NOTEBOOK, ENTER ipython kernel install --user --name=mental_health_env
7. TO USE ENVIRONMENT, OPEN JUPYTER NOTEBOOK FROM CLUSTER, HIT 'New' IN THE TOP RIGHT CORNER, AND CHOOSE THE CREATED KERNEL


INSTRUCTIONS FOR UPDATING THE CONDA ENVIRONMENT TO BE COMPATIBLE WITH THE NAIVE BAYES CLASSIFIER (!!IMPORTANT!!)

1) conda env list (run this to make sure you're in the right location)
2) conda activate mentalhealth (or whatever the name of your environment is, see above step)
3) conda verify (run after every install to make sure it worked!)
(Also order of installs matter since you need numpy for pandas, and matplotlib)
4) conda install numpy
5) conda install pandas
6) conda install matplotlib
7) conda install pip
8) pip install textblob
9) conda install scikit-learn