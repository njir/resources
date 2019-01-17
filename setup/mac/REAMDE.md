# 개발환경 설정
- install [spectacle](https://www.spectacleapp.com), [alfred](http://alfredapp.com)
- [본격 macOS에 개발 환경 구축하기](https://subicura.com/2017/11/22/mac-os-development-environment-setup.html)
- 기존 설정에서 아래 프로그램 or 플러그인 설치
  - zsh-syntax-highlighting
  - zsh-autosuggestions
  - neovim
  - SpaceVim 
  - fzf
  - fasd
  - tmux
  - tmuxinator
  	- https://gist.github.com/colmarius/f8c0c824b87db9279222
  - tig
  - thefuck
  - [jq](https://blog.outsider.ne.kr/1202)
  
- 3분의1 개발환경 설정
	- install yarn
	```
  $ brew install yarn
  ```
  - tslint 설정
  ```
  # Install the global CLI and its peer dependency
  $ yarn global add tslint typescript
  # Navigate to to yoursls dynamodb installrces folder
  $ cd path/to/project
  # Lint TypeScript source globs
  $ tslint -c tslint.json 'src/**/*.ts'
  ```
  - serverless 설치
  ```
  # Installing the serverless cli
  $ npm install -g serverless
  $ sls dynamodb install
  ```
  - awscli 설지
  ```
  $ brew install awscli
  ```
  - angular cli 설치
  ```
  $ npm install -g @angular/cli
  ```
  - start serverless
  ```
  $ serverless offline start --migrate
  ```
  - insert dynamodb

```
// insert metadata 
var params = {
    TableName: 'products',
    Item: {
        productId: '1',
        item: 0
    }
};

ppJson(params);
docClient.put(params, function(err, data) {
    if (err) ppJson(err); // an error occurred
    else console.log("PutItem returned successfully");
});
```


### tmux: 여러개의 터미널을 실행할 수 있는 TTY 멀티플렉서 
- [tmux 입문자 시리즈 요약](http://www.haruair.com/blog/2124)
- [Tmux and Vim - even better together](https://blog.bugsnag.com/tmux-and-vim/?utm_source=hackernewsletter&utm_medium=email&utm_term=fav)
- [dotfiles](https://github.com/keeganlow/dotfiles)
