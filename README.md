# Windows安裝Pyenv
PS C:\Windows\system32> Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"

# 安裝Python版本
pyev install 3.8.12

# 安裝虛擬環境指令
pip install virtualenv

## 遇到SSL驗證問題，跳過驗證
pip install virtualenv --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host=files.pythonhosted.org

