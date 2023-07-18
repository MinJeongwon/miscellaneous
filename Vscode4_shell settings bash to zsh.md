## (원격) 기본 쉘을 zsh로 설정하기

<br>

1. vscode에서 ssh 호스트 구성 열기

2. 호스트 등록 시 `SetEnv` 추가
    ```console
    Host 원격 이름
        HostName 원격 아이피
        User 원격 유저명
        SetEnv TERM=/usr/local/bin/zsh 
    ```

3. 원격의 bashrc에 아래 내용 추가
    ```console
    if [[ "$TERM_PROGRAM" == "vscode" ]]; then
        # ~/.profile is run by the login shell (this is what ssh uses)
        # ~/.bashrc is run by the interactive shell (this is what vscode uses)
        # Therefore, we only need to change the shell to zsh here since
        # vscode will run ~/.bashrc for us.
        exec zsh -l
    fi
    ```

4. shell integration failed to activate라는 문구가 뜨는 경우    
    ➜ vscode settings에서 setting.json을 열어 아래 내용 추가
    ```console
    "terminal.integrated.shellIntegration.enabled": false
    ```
    ➜ 원격의 .zshrc에 아래 내용 추가
    ```console
    [[ "$TERM_PROGRAM" == "vscode" ]] && . "$(code --locate-shell-integration-path zsh)"
    ```

<br>

참고 : [기본 쉘을 zsh로 설정하기](https://stackoverflow.com/questions/70824431/integrated-shell-changes-back-to-bash-every-time-i-open-remote-workspace)      
[원격 환경 shell integration failed to activate](https://stackoverflow.com/questions/73292777/vscode-ssh-remote-connected-to-ec2-instance-shell-integration-failed-to-activa)
