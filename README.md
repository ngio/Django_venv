
# Vscode에서 Django 사용하기

https://velog.io/@tett_77/Vscode%EC%97%90%EC%84%9C-Django-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0



# Visual-Studio-Code에서-Django-프로젝트-기본-셋팅-하는-법


https://velog.io/@rjsekaehdhkw/Visual-Studio-Code%EC%97%90%EC%84%9C-Django-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%EA%B8%B0%EB%B3%B8-%EC%85%8B%ED%8C%85-%ED%95%98%EB%8A%94-%EB%B2%95


VSCODE에서 Django 실행하기 


Ctrl + ` 을 눌러서 터미널 창을 열어줍니다.


가상환경 생성 - 아래 코드를 터미널에 입력하면 python 자체적으로 가지고 있는 가상환경을 설치해줍니다.

    python -m venv  venv(원하는 가상환경 이름)


(venv) D:\_py_django>./venv/Scripts/activate 

또는 

(venv) D:\_py_django>call venv\Scripts\activate



가상환경 종료는  
(venv) D:\_py_django>deactivate 

 

    git init
    
    git remote add origin [Github repository 주소] 
    
    git add .
    
    git commit -m '설명'
    
    git branch -M main
    
    git push origin main


* 뭔 에러인가?
  
           ! [rejected]        main -> main (fetch first)
          error: failed to push some refs to 'https://github.com/ngio/Django_venv.git'
          hint: Updates were rejected because the remote contains work that you do not
          hint: have locally. This is usually caused by another repository pushing to
          hint: the same ref. If you want to integrate the remote changes, use
          hint: 'git pull' before pushing again.
          hint: See the 'Note about fast-forwards' in 'git push --help' for details.

* 해결 방법
원격 저장소의 최신 내용을 가져옵니다.

      git pull origin main --rebase
      
      git add .
      git rebase --continue
      
      git push origin main



git pull origin main --rebase 대신 git pull origin main을 사용할 수도 있지만, --rebase가 병합 충돌을 더 깔끔하게 처리합니다.
강제 푸시는 가능하면 지양하고, pull --rebase를 활용하는 것이 좋습니다.


