# Start the project
1- Fork the repo
2- clone the repo
`` bash
git clone https://github.com/tamer-elkoT/carrier-sla-risk-intelligence-model.git
``
3- Create a branch for week 1
`` bash
git checkout -b feature/week1-data-preprocessing
``

we will have a branch for each week 
# branches
- feature/week1-data-preprocessing
- feature/week1-feature-engineering
- feature/week1-model-training
- feature/week1-explainability-shap

# create a virtual environment


cd ~/carrier-sla-risk-intelligence
source .venv/bin/activate
pip install pandas numpy jupyter notebook
pip freeze > requirements.txt