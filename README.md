# Movation

I have several programs written in [Python](https://www.python.org/) and [Java](https://openjdk.java.net/).
They are all simple things that mearly start, then run to compleation.
Normally I will RDP into one of my local servers and run the command.
When my local servers hit capacity, I would like to be able to expand a hybrid cloud to Azure or AWS.

# Goals

* Have a single codebase for locally running the programs
* Matain source code confidentually
* Matain configuration file confidentually


# Tool Chain

* [GitHub](https://github.com)
* [Chocolatey](https://community.chocolatey.org)
* [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install)
* VS Code
* [Docker Desktop](https://www.docker.com/products/docker-desktop)

Open an _Admin_ Powershell and run the following:

01. Install Windows Subsystem for Linux
    ```{ps1}
    wsl --install
    ```
02. Install Chocolatey
    ```{ps1}
    if('Unrestricted' -ne (Get-ExecutionPolicy)) { Set-ExecutionPolicy Bypass -Scope Process -Force }
    iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
    refreshenv
    ```
03. Install VS Code, Docker via Chocolatey
    ```{ps1}
    choco install vscode docker-desktop -y 
    ```
