# Usage
1. **Install** 
    ```
    git clone git@github.com:jinmiaoluo/v2ray-core-helper.git ~/.proxy
    ```

2. **Setup**

    If you use bash shell 
    ```
    echo 'export PATH="$PATH:$HOME/.proxy"' >> ~/.bash_profile
    ```
    
    **[option]** If you use zsh shell 
    ```
    echo 'export PATH="$PATH:$HOME/.proxy"' >> ~/.zshrc
    ```
    
    Setup property permission
    ```
    sudo sh -c 'echo "$(whoami) ALL = (ALL) NOPASSWD:/usr/sbin/networksetup" >> /etc/sudoers' 
    ```
3. **Restart your shell**
    ```
    exec $SHELL
    ``` 
4. **Download dependency**
    ```
    proxy init
    ```

5. **Add your outbounds**
    
    Add your outbounds settings into [config.json](./config.json)

5. **Start your proxy**
    ```
    proxy start
    ```
    
6. **Figure out more usage**
    ```
    proxy help
    ```

7. **[option] Setup terminal proxy**
    
    if you use bash shell
    ```
    echo -e "export http_proxy='http://127.0.0.1:9090'\nexport https_proxy='http://127.0.0.1:9090'" >> ~/.bash_profile
    ```
    if you use zsh shell 
    ```
    echo -e "export http_proxy='http://127.0.0.1:9090'\nexport https_proxy='http://127.0.0.1:9090'" >> ~/.zshrc
    ```
    
8. **[option] Temporarily unset terminal proxy**
    ```
    unset http_proxy && unset https_proxy
    ```

9. **[option] Persistently unset terminal proxy**
    
    delete the follow lines in your `.bash_profile` or `.zshrc`
    ```
    export http_proxy='http://127.0.0.1:9090'
    export https_proxy='http://127.0.0.1:9090'
    ```