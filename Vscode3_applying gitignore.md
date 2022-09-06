## .gitignore가 적용되지 않을 때

<br>

```console
git rm -r --cached .
git add .
git commit -m "remove source files"
```

참고 : [git ignore가 적용이 안될 때](https://novemberfirst.tistory.com/91#:~:text=git%EC%9D%98%20%EC%BA%90%EC%8B%9C%EB%AC%B8%EC%A0%9C%20%EC%9D%B4%EB%AF%80%EB%A1%9C,%ED%9B%84%20%EB%8B%A4%EC%8B%9C%20%EC%BB%A4%EB%B0%8B%ED%95%98%EB%A9%B4%20%EB%90%9C%EB%8B%A4.&text=%EC%82%AC%EC%9D%B4%ED%8A%B8%EC%97%90%20%EB%93%A4%EC%96%B4%EA%B0%80%EC%84%9C%20%ED%98%84%EC%9E%AC%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8,%EC%9C%BC%EB%A1%9C%20%EB%82%B4%EC%9A%A9%EC%9D%84%20%EB%A7%8C%EB%93%A4%EC%96%B4%20%EC%A4%80%EB%8B%A4.) 
