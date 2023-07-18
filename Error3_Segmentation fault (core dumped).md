## 5357 segmentation fault (core dumped)  python ______.py

<br>

multi GPU 사용을 위해 DataParallel 처리를 해주었을 때 종종 발생하는 오류   
➜ model에 대한 함수 사용 시 중간에 `module`을 추가해주기

'DataParallel' object has no attribute 'config'라는 오류가 발생한 경우     
1. 해당 라인 찾아가기
   ```python
   masked_lm_loss = loss_fct(prediction_scores.view(-1, model.config.vocab_size)

   File "/home/jwmin/anaconda3/envs/BERT_FP/lib/python3.8/site-packages/torch/nn/modules/module.py", line 947, in __getattr__
   raise AttributeError("'{}' object has no attribute '{}'".format
   AttributeError: 'DataParallel' object has no attribute 'config'
   ```   

2. model과 해당 함수 사이에 `module` 추가해주기
   ```python
   masked_lm_loss = loss_fct(prediction_scores.view(-1, model.module.config.vocab_size)
   ```   

<br>

출처 : https://biology-statistics-programming.tistory.com/142  
