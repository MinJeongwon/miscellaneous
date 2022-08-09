## oh my zsh 사용하기

<br>

1. zsh 설치     
   ```console
   sudo apt-get install zsh   
   ```   

2. 기본 쉘을 zsh로 바꾸는 명령
   ```console
   chsh -s /usr/bin/zsh
   ```

3. curl과 git 설치
   ```console
   sudo apt-get install curl
   sudo apt-get install git
   ```

4. oh my zsh 설치
   ```console
   sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
   ```

5. 테마를 agnoster로 변경
   ```console
   sudo vim ~/.zshrc
   # ZSH_THEME=”robbyrussell” 
   ZSH_THEME=”agnoster”
   ```

6. 테마를 `powerlevel10k`로 변경
   ```console
   git clone https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
   sudo vim ~/.zshrc
   # ZSH_THEME=”robbyrussell” 
   # ZSH_THEME=”agnoster”
   ZSH_THEME="powerlevel10k/powerlevel10k"
   ```

7. powerlevel10k configuration wizard 다시 실행하고 싶은 경우 
   ```console
   p10k configure
   ```
   
8. 폰트 깨지는 경우 폰트 다운 후 변경
   ```console
   git clone https://github.com/powerline/fonts.git
   #폰트 설치
   cd fonts
   ./install.sh
   ```

9. 터미널 폰트 변경     
   터미널 우측 마우스 클릭 -> preferences -> 폰트를 `Ubuntu Mono derivative Powerline Regular`로 변경

<br>

참고자료 : http://programmingskills.net/archives/115    
참고자료 : https://velog.io/@oklfg2002/OS-X-Linux-WSL2-%ED%84%B0%EB%AF%B8%EB%84%90%EC%9D%84-%EA%BE%B8%EB%A9%B0%EB%B3%B4%EC%9E%90    
참고자료 : https://github.com/romkatv/powerlevel10k
