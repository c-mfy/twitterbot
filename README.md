
my steps:
1. installed pyenv-win because tweepy doesn't use the latest version of python, and the official python website doesn't have older version download links anymore
- in Windows PowerShell, "Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine"
- in Windows PowerShell, "Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1""
- Configure paths:
PS C:\WINDOWS\system32> [System.Environment]::SetEnvironmentVariable('PYENV', $env:USERPROFILE + "\.pyenv\pyenv-win\","User")
PS C:\WINDOWS\system32> [System.Environment]::SetEnvironmentVariable('PYENV_ROOT', $env:USERPROFILE + "\.pyenv\pyenv-win\","User")
PS C:\WINDOWS\system32> [System.Environment]::SetEnvironmentVariable('PYENV_HOME', $env:USERPROFILE + "\.pyenv\pyenv-win\","User")
PS C:\WINDOWS\system32> [System.Environment]::SetEnvironmentVariable('path', $env:USERPROFILE + "\.pyenv\pyenv-win\bin;" + $env:USERPROFILE + "\.pyenv\pyenv-win\shims;" + [System.Environment]::GetEnvironmentVariable('path', "User"), "User")
- in CMD, pyenv install 3.11.0 to install that version of Python
- in CMD, pyenv global 3.11.0 to set the version
  
2. install tweepy API, "pip install tweepy"
