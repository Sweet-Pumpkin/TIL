## Error&Solution

### [ReactDOM.render 에러 현상](https://velog.io/@sweet_pumpkin/Error-ReactDOM.render%EB%8A%94-React18%EC%97%90%EC%84%9C-%EC%A7%80%EC%9B%90%EB%90%98%EC%A7%80-%EC%95%8A%EC%8A%B5%EB%8B%88%EB%8B%A4)
`ReactDOM.render()`를 실행했을때 아래와 같은 경고 메세지가 콘솔창에 나타나는 문제.
```
Warning: ReactDOM.render is no longer supported in React 18. Use createRoot instead. Until you switch to the new API, your app will behave as if it's running React 17.
```
2022년 3월 29일에 출시된 React18 환경에서는 `ReactDOM.render()`가 사용되지 않기 때문에 버전에 맞는 코드를 업데이트 해야 한다.

---

### [git flow release 에러 현상](https://velog.io/@sweet_pumpkin/Error-%EB%8B%BF%EC%9D%84%EB%93%AF-%EB%A7%90%EB%93%AF-%EB%8B%BF%EC%A7%80-%EC%95%8A%EB%8A%94-%EB%B8%8C%EB%9E%9C%EC%B9%98...-%EC%96%B4%EB%94%94%EC%84%9C%EB%B6%80%ED%84%B0-%EC%9E%98%EB%AA%BB%EB%90%9C-%EA%B2%83%EC%9D%B8%EA%B0%80)
`$ git flow release finish v0.1 ` 이후 _release_ 브랜치와 _main_ 브랜치가 병합되지 않고 아래와 같은 에러 메세지가 나타나는 문제.
```
fatal: 'release' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```
_main_ 브랜치와 _develop_ 브랜치가 서로 연결되어 있지 않아 생기는 문제. _main_ 브랜치와 _develop_를 연결시켜줘야 한다.

---

### [git 명령어 에러 현상](https://velog.io/@sweet_pumpkin/Error-Git-push-%EA%B1%B0%EC%A0%88-%ED%95%B4%EA%B2%B0)
`$ git push -u origin develop` 명령어를 입력했으나, 아래와 같은 에러 메세지가 나타나며 깃허브에 코드가 업로드 되지 않는 문제.
```
$ git push -u origin develop
remote: Permission to qjagkrdldi/lotto_create.git denied to Sweet-Pumpkin.
fatal: unable to access 'https://github.com/qjagkrdldi/lotto_create.git/': The requested URL returned error: 403
```
_origin_으로 등록된 주소가 포크해온 주소가 아닌, 같이 프로젝트를 만드는 팀원의 주소로 등록되어 생긴 문제. 포크 해온 주소로 재등록해야 한다.