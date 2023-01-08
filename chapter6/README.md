# ToDo
- [ ] 以下のコード理解（模範解答にあった）
    * `idata_l`は、pm.sample実行次の`return_inferencedata=True`指定によって得られたもの
```
α_l_post = idata_l.posterior['α'].mean(("chain", "draw")).values
```
- [ ] LOO, WAICの違いの解釈
- [ ] 情報量基準のプロットまで
```
cmp_df = az.compare({'model_l':idata_l, 'model_p':idata_p},
                    method='BB-pseudo-BMA', ic="waic", scale="deviance")
```

- [ ] ベイズファクター計算の問題点に関する理解
    * ２モデルのサンプリング比が変わり、片方のモデルのパラメータも更新される状態は残り続ける。