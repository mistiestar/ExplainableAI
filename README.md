# ExplainableAI: README

SHAP_v_CFSHAP_example.ipynb is a jupyter notebook showing the use case and plots as described in the report.

1. The data set used in this report can be found here:
University of California, Irvine, Machine Learning Repository. (1994, November 16). Statlog
(German Credit Data). https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data

2. The package used to generate counterfactual SHAP (CF-SHAP) explanations can be found here:
https://github.com/jpmorganchase/cf-shap/tree/main

Authors:
Albini, E., Long, J., Dervovic, D., & Magazzeni, D. (2022). Counterfactual Shapley Additive Explanations.
Proceedings of the ACM Conference on Fairness, Accountability, and Transparency (FAccT '22).
https://doi.org/10.1145/3531146.3533168

Note, the package not been updated for 4 years, and therefore requires a much older version of python and its libraries. The work-around I found is to create a virtual anaconda environment that uses python v3.8 (the version used by the authors). To do so, see the code below:

\# create virtual environment called "cfshap"

conda create -n cfshap python=3.8 -y
conda activate cfshap

\# install all the required versions of libraries as described by requirements.txt of the package

pip install numpy==1.19.2 pandas==1.1.5 scikit-learn==0.24.2 shap==0.39.0 xgboost==1.3.3 joblib==1.0.1 tqdm==4.61 numba==0.51.2 cached_property dataclasses typing_extensions

\# open jupyter notebook

conda install notebook
jupyter notebook
