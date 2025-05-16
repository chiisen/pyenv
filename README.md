# pyenv
使用 pyenv 管理 Python 環境

---

# 使用 git clone 安裝 pyenv 
```shell
git clone https://github.com/pyenv-win/pyenv-win.git "$HOME/.pyenv"
```

# 使用 PowerShell 來設定環境變數(一次就行了)：
```shell
[System.Environment]::SetEnvironmentVariable('PYENV',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
[System.Environment]::SetEnvironmentVariable('PYENV_HOME',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
[System.Environment]::SetEnvironmentVariable('path', $env:USERPROFILE + "\.pyenv\pyenv-win\bin;" + $env:USERPROFILE + "\.pyenv\pyenv-win\shims;" + [System.Environment]::GetEnvironmentVariable('path', "User"),"User")
```

# 確認 pyenv 安裝的版本：
```shell
pyenv --version
```

# versions | 檢視所有可選用的 python 版本
```shell
pyenv versions
```

# install -l | 檢視可以安裝版本的 python
```shell
pyenv install -l
```

# install | 安裝特定版本的 python
```shell
pyenv install 3.5.2
```

# local | 設定特定專案使用特定版本 python
```shell
pyenv local 3.5.2
```

# global | 設定全域環境所使用特定版本 python
```shell
pyenv global 3.5.2
```

# rehash | 更新 python 環境資訊
如果有使用 pip 安裝或解安裝 library 以及異動特定 version Python 的資料夾內容，必須使用 rehash 通知 pyenv 重新對應相關的使用連結。
```shell
pyenv rehash
```
