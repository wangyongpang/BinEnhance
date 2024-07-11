# BinEnhance<br>

################################################<br>
**This is where BinEnhance's code and data are stored**<br>
################################################<br>
[Eval]For now, considering the high coupling of the current code, only the code and data needed for the evaluation experiments and the code of the model in the paper have been released, and the complete code and data will be released gradually:<br>

1. Install the required environment, the python environment we use is python3.8<br>

```python
pip install -r Requirements.txt
```

2. Download the evaluation dataset from [OneDrive](https://1drv.ms/u/s!AuV8PQVWsJ_qgSwEwUZBNlVjlzUC?e=K3ryoH):<br>

   This evaluation dataset contains embeddings of all test binary functions generated by the five methods used in the paper (HermesSim[^1], TREX[^2], Asteria[^3], Asm2vec[^4], Gemini[^5]), as well as all embeddings enhanced by BinEnhance. There are 13 folders after unpacking the evaluation dataset. `Asm2vec` and `Asm2vec+BinEnhance` are the embedding files generated by the original method and BinEnhance. The other models are similar. `Eval_datas` is the evaluation function pool (from Dataset $D1$ and $D2\_norm$) of different models. `RDFs` is all functions' readable data features. `save_models` is our trained model. <br>

3. Use the storage path of the evaluation dataset downloaded in step 2 to run Eval.py<br>

```python
python Eval.py --data-path="xxx/Eval" --dataset=2<br>
```

################################################<br>
**Datasets**<br>
################################################<br>
**$D1$ in the paper**: After communicating with the Asteria author, this dataset will be released later.<br>

**$D2<u>_</u>{norm}$ and $D2<u>_</u>{noinline}$ in the paper (The homologous function pairs for the evaluation of the function inline scenario can be constructed from them)**: These datasets can download from [normal_dataset](https://drive.google.com/file/d/1K9ef-OoRBr0X5u8g2mlnYqh9o1i6zFij/view) and [noinline_dataset](https://drive.google.com/file/d/1wt7GY-DDp8J_2zeBBVUrcfWIyerg_xLO/view) in [Binkit](https://github.com/SoftSec-KAIST/BinKit).<br>

**$D3<u>_</u>{firmware}$**: The firmware dataset will be released in the future due to its large size.<be>


################################################<br>
**References**<br>
################################################<br>

[^1]: H. He, X. Lin, Z. Weng, R. Zhao, S. Gan, L. Chen, Y. Ji, J. Wang, and Z. Xue, “Code is not natural language: Unlock the power of semanticsoriented graph representation for binary code similarity detection,” in 33rd USENIX Security Symposium (USENIX Security 24), PHILADELPHIA, PA, 2024. 
[^2]: K. Pei, Z. Xuan, J. Yang, S. Jana, and B. Ray, “Learning approximate execution semantics from traces for binary function similarity,” IEEE Transactions on Software Engineering, vol. 49, no. 4, pp. 2776–2790, 2022.
[^3]: S. Yang, L. Cheng, Y. Zeng, Z. Lang, H. Zhu, and Z. Shi, “Asteria: Deep learning-based ast-encoding for cross-platform binary code similarity detection,” in 2021 51st Annual IEEE/IFIP International Conference on Dependable Systems and Networks (DSN). IEEE, 2021, pp. 224–236.
[^4]: S. H. Ding, B. C. Fung, and P. Charland, “Asm2vec: Boosting static representation robustness for binary clone search against code obfuscation and compiler optimization,” in 2019 IEEE Symposium on Security and Privacy (SP). IEEE, 2019, pp. 472–489. 
[^5]: X. Xu, C. Liu, Q. Feng, H. Yin, L. Song, and D. Song, “Neural network based graph embedding for cross-platform binary code similarity detection,” in Proceedings of the 2017 ACM SIGSAC conference on computer
and communications security, 2017, pp. 363–376. 


