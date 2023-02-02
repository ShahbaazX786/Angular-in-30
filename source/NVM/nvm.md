## NVM: Node Version Manager
- NVM is a tool which helps us in installing and managing multiple or all node versions in our pc with very much less hassle.
- In conventional method you install nodejs via a exe file and it will have a version say 15.
    - Now If you want to have another version of node (due to some project requirements) and you can't do it unless you uninstall the old node version 15 first.
    - There is also an option to install in different locations but it is risky and may lead to unexpected errors and behaviour.
- So to avoid all these hassle of downloading and installing node via exe packages you can just do so by using NVM.

#### Steps to install(on Windows):
- Go to this [Readme](https://github.com/coreybutler/nvm-windows#readme) and follow the complete guide or just Click on [Download Now](https://github.com/coreybutler/nvm-windows/releases) button, scroll down and click on nvm-setup.exe and install it.
- Restart your PC.
#### Steps to install(on Unix):

##### 1.Run the installer via CLI:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
or
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
- You can use <code>curl</code> or  <code>bash</code> depending on the command available on your device.
- These commands will clone the nvm repository to a  <code>~/.nvm</code> directory on your device.

##### 2.Update your profile config:
- The installation process from step 1 should also automatically add the nvm configuration to your profile.
- If you're using zsh, that would be ```~/.zshrc.```
- If you're using bash, that would be ```~/.bash_profile...``` or some other profile.

- If it doesn't automatically add nvm configuration, you can add it yourself to your profile file:
- This command below loads nvm for use.

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

##### 3.Reload the shell config:
- Now run the below command to reload the configs made so that nvm is ready to use via terminal.
```
source ~/.bashrc
```
- If you want you can restart your system(mac).

>Note: run **nvm -v** to ensure you see some nvm version and clear that final doubt whether nvm is correctly installed or not.


#### Some useful nvm commands:
- <code>nvm list</code> - lists all node versions available in your pc.
- <code>nvm list lts</code> - lists all available  long term support nodejs versions
- <code>nvm list available</code> - lists all available nodejs versions
- <code>nvm install 15.0.0</code> - downloads and install the nodejs version 15.0.0.
- <code>nvm install lts</code> - downloads and install the latest available long term support(LTS) node version.
- <code>nvm install latest</code> - downloads and install the latest available node version.
- <code>nvm uninstall 15.0.0</code> - uninstalls the specified node version.
- <code>nvm use 15.0.0</code> - sets the current node version to 15.0.0.

>These commands are same for all OS.