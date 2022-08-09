## syntax highlighting과 autosuggestions 설치

1. syntax highlighting, autosuggestions 설치
   ```console
   git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
   git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
   ```

2. zshrc 편집
   ```console
   vim ~/.zshrc
   ```

3. 아래 내용 추가
   ```console
   plugins=(
    git
    zsh-syntax-highlighting
    zsh-autosuggestions
    )

4. zshrc 설정 저장
   ```console
   source ~/.zshrc
   ```

<br>

참고자료 : https://velog.io/@ruddms936/zsh-%ED%94%8C%EB%9F%AC%EA%B7%B8%EC%9D%B8-%EC%84%A4%EC%B9%98








