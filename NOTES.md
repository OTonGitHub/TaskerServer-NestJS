## Node/Nest/NVM Commands

- setup nvm https://github.com/coreybutler/nvm-windows/releases
- install node
  - `nvm install lts`
  - `nvm use lts`
- setup NestJS Project:
  - `npm i -g @nestjs/cli`
  - `nest --version`
  - `nest --help`
  - `mkdir <name> && cd <name>`
  - `nest new .`
  - refer to _package.json_ and run `npm run start`
  - getting error on importing @nestjs/core, so ran `npm install` <- likely because cloned
  - for hot-reload `npm run start:dev`
- #### Code Generation
  - `nest generate controlloer` -> `nest g co`
  - use `--no-spec` to avoid testing file generation
  - `nest generate controller modules/abc` -> will generate controller in src/modules/abc

## Git w/SSH

git checkout -- .
git clean -fd

- creating ssh keys

  - `mkdir ~/.ssh && cd ~/.ssh`
  - `ssh-keygen -t ed25519 -C "email@email.email" -f OTonGitHub`

- add to ssh-agent

  - ``eval `ssh-agent` ``
  - `ssh-add OTonGitHub`
  - `ssh-add -l`

- now you can `cat OTonGithub.pub` and place the file in https://github.com/settings/keys

- then test the configuration

  - `ssh -T git@OTonGitHub`

- ### New Repo

  - `git init`
  - `git config user.name "OTonGitHub"`
  - `git config user.email email@email.email`
  - `git add .`
  - `git commit -am "init commit"`
  - `git branch -M main`
  - `git remote add origin https://github.com/OTonGitHub/Temp.git`
  - `git push -u origin main`

- ### Cloning Existing

  - `git clone <https_link>`
  - `git remote -v`
  - `git remote set-url origin git@OTonGithub:OTonGitHub/repo.git`
  - `git push`

## Just Notes

- Decided to name controllers pluran
