# pymc3-bayes-modeling-book
Pythonによるベイズ統計モデリングの勉強録

# 環境構築（フロムスクラッチの手順）
1. condaで適当な仮想環境を作る。python versionのみ指定する。
1. `pip install pymc3` 
    * -> 最新が入る（githubのtagなどをみて、バージョン指定するなどしても良い）
1. `pip install jax jaxlib numpyro` 
    * -> requirements.txt参照
    * しかしこれでまだスピードアップしたわけではなさそう。結構時間がかかってる気がする。
1. `conda install -n [環境名] ipykernel --update-deps --force-reinstall`

## 環境構築の再現
- まだ試したことないが、以下でいけるのでは。
- ※ファイル中の`prefix`のみ修正の必要あり
```
conda env create -f environment_pymc3_latest.yml
```
