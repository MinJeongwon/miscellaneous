## torch.distributed 디버깅

<br>

1. vscode 디버깅을 위한 launch.json 세팅

2.  e.g.     
   `python -m torch.distributed.launch --nproc_per_node=1 main_swav.py \
--data_path /dataset/imagenet/train \`     
를 디버깅하고자 할 때
    ```console
    {
            "version": "0.2.0",
            "configurations": [
                {
                    "name": "Python: Current File",
                    "type": "python",
                    "module": "torch.distributed.launch",
                    "request": "launch",
                    "console": "integratedTerminal",
                    "args": [
                        "--nproc_per_node", "1", 
                        "main_swav.py",
                        "--data_path", "/dataset/imagenet/train",
                        ]
                }
            ]
    }
    ```

    * module을 명시 : `"module": "torch.distributed.launch"`
    * 그 외의 것들은 `"args": []`에 넣기
    * python -m flag는 무시해도 됨

<br>

참고 : [How to make VScode launch.json for a Python module](https://stackoverflow.com/questions/67518928/how-to-make-vscode-launch-json-for-a-python-module) 
