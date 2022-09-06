## TypeError: Descriptors cannot not be created directly (protoc >= 3.19.0)

<br>

Tensorflow, Tensorboard, 등과 protobuf의 버전이 맞지 않아서 발생하는 오류.    
➜ TensorFlow 나 PyTorch 버전을 올리면 해결 가능!

1. Tensorflow를 2.9.1 이상으로 올리기
   ```console
   pip install tensorflow==2.9.1
   ```
   or     
   protobuf 버전을 낮추기
   ```console
   pip install –upgrade protobuf<=3.20.1     
   or 
   pip install protobuf<=3.20.1 --force-reinstall
   ```   

2. 코드 실행

<br>

출처 : https://hello-bryan.tistory.com/428 
