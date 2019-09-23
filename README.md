# v2ray-core-helper
A simple (pure bash script) command line installer and controller for [v2ray-core](https://github.com/v2ray/v2ray-core).

**Note**: Default config is Chinese area improved for solving the problem causing by Chinese Great Firewall. You should modify it by yourself if you dont live in China.

# Table of Contents

<!-- vim-markdown-toc GFM -->

* [Usage](#usage)
  * [setup](#setup)
  * [advanced](#advanced)

<!-- vim-markdown-toc -->

# Usage
## setup
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

3. **Setup property permission**

    ```
    sudo sh -c 'echo "%admin ALL = (ALL) NOPASSWD:/usr/sbin/networksetup" >> /etc/sudoers'
    ```

4. **import shell config**

    If you use bash shell
    ```
    source ~/.bash_profile
    ```

    **[option]** If you use zsh shell
    ```
    source ~/.zshrc
    ```
5.  **Add your outbounds**

    Add your outbounds settings into [config.json](https://github.com/jinmiaoluo/v2ray-core-helper/blob/401463947270acf40069ac6c9be5462843ca2817/config.json#L60)

6. **Download dependency**
    ```
    proxy init
    ```

7. **Start your proxy**
    ```
    proxy start
    ```
    Done! You can visit google now. Open Safari and try it yourself.

## advanced
1. **[option] Setup terminal proxy**

    If you use bash shell
    ```
    echo -e "export http_proxy='http://127.0.0.1:9090'\nexport https_proxy='http://127.0.0.1:9090'" >> ~/.bash_profile && source ~/.bash_profile
    ```
    **[option]** If you use zsh shell
    ```
    echo -e "export http_proxy='http://127.0.0.1:9090'\nexport https_proxy='http://127.0.0.1:9090'" >> ~/.zshrc && source ~/.zshrc
    ```

2. **[option] Temporarily disable terminal proxy**

    ```
    unset http_proxy && unset https_proxy
    ```

3. **[option] Persistently disable terminal proxy**

    delete the follow lines in your `.bash_profile` or `.zshrc`
    ```
    export http_proxy='http://127.0.0.1:9090'
    export https_proxy='http://127.0.0.1:9090'
    ```

4. **[option] Figure out more usage**

    ```
    proxy help
    ```
