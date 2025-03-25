# Windows安裝Pyenv
PS C:\Windows\system32> Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"

## 安裝Python版本
pyev install 3.8.12

## 安裝虛擬環境指令
pip install virtualenv

### 遇到SSL驗證問題，跳過驗證
pip install virtualenv --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host=files.pythonhosted.org

如果要一次設定完，避免每次都要輸入，移動至 \.pyenv\pyenv-win\versions\3.8.12\Scripts 或虛擬環境 \3.8.12\Scripts 建立 pip.ini，輸入下列設定：
```
[global]
trusted-host = pypi.org
             pypi.python.org
             files.pythonhosted.org
```

## 建立特定Python版本的虛擬環境在venv統一管理
mkdir venv
cd venv
virtualenv 3.8.12

## 啟動虛擬環境
.\3.8.112\Scripts\activate

## 關閉虛擬環境
deactivate
