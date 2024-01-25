## startup
```bash
docker-compose up -d
```

## Work with Notebook
open the http://localhost:8888/ in your browser to view the notebook.


## Evaluation

Metrics: 

Root-mean-square error = 0.9567427744947872
Mean absolute error = 0.7423525855668276
R2 score = 0.2709882370597655
Explained variance = 0.672904484834605

on my model whose hyperparametars are:
RANK = 10
MAX_ITER = 15
REG_PARAM = 0.05

Later on with brute-force grid search and hyperparametars:
Rank range from 4 to 21
MaxIter in [10, 15, 20]
RegParam in [0.05, 0.1, 0.15]

given as parametars in als which is an instance of ALS-alternating least squares(from pyspark.ml.recommendation import ALS)

I found out that best RMS error has a model with parameters: rank=5, maxIter=20, regParam=0.1
