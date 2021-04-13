Repository contains the code for 2nd place solution of [VinBigData Chest X-ray Abnormalities Detection](https://www.kaggle.com/c/vinbigdata-chest-xray-abnormalities-detection/leaderboard) 
competition. The goal of competition was to automatically localize and classify 
thoracic abnormalities from chest radiographs.

## Details

Solution consists of 3 parts. Each part is models from each team member. Predictions of each part in the end ensembled in single 2nd place submission on LeaderBoard. 
You can use only inference or train models from scratch.   

## Only inference 

```
cd part_zfturbo
pip install -r requirements.txt
sh ./preproc.sh
sh ./inference.sh
cd ..

cd part_ivan
sh ./setup.sh
sh ./preproc.sh
sh ./inference.sh
cd ..

cd part_sergey
sh ./inference.sh
cd ..

python3 ensemble_models.py
```

## Train

```
cd part_zfturbo
pip install -r requirements.txt
sh ./preproc.sh
sh ./train.sh
sh ./inference.sh
cd ..

cd part_ivan
sh ./setup.sh
sh ./preproc_train.sh
sh ./train.sh
sh ./inference.sh
cd ..

cd part_sergey
sh ./train.sh
sh ./inference.sh
cd ..

python3 ensemble_models.py
```
