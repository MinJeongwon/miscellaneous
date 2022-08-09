## 터미널 실행 시 자동으로 conda base가 실행되도록 하기

<br>

1. bashrc 편집해주기      
    
   ```console
   vim ~/.bashrc
   ```

2. bashrc 설정 파일에 아래 내용 추가하기
   ```console
   # >>> conda initialize >>>
   # !! Contents within this block are managed by 'conda init' !!
   __conda_setup="$('/home/jwmin/anaconda3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
   if [ $? -eq 0 ]; then
       eval "$__conda_setup"
   else
       if [ -f "/home/jwmin/anaconda3/etc/profile.d/conda.sh" ]; then
           . "/home/jwmin/anaconda3/etc/profile.d/conda.sh"
       else
           export PATH="/home/jwmin/anaconda3/bin:$PATH"
       fi
   fi
   unset __conda_setup
   # <<< conda initialize <<<
   ```

3. 변경사항 적용하기     
   cf. `source` 명령어는 스크립트 파일을 수정한 후에 수정된 값을 바로 적용하기 위해 사용하는 명령어     
   [(출처)](https://klero.tistory.com/entry/source-%EB%AA%85%EB%A0%B9%EC%96%B4%EB%9E%80)  
   ```console
   source ~/.bashrc
   ```

