# weechat

## Introduction

My [weechat](https://weechat.org/) configuration.  I generally only use [freenode](https://freenode.net/) and authenticate using SASL, so settings reflect that.

This configuration relies on weechat's [secure data](https://www.weechat.org/files/doc/stable/weechat_user.en.html#secured_data) feature.  To set-up secure data, follow these steps:

1. Create `~/.weechat/sec.conf` and fill in your freenode nickname and SASL password.

    ```
    #
    # weechat -- sec.conf
    #

    [crypt]
    cipher = aes256
    hash_algo = sha256
    passphrase_file = ""
    salt = on

    [data]
    __passphrase__ = off
    freenode_sasl_password = "YOUR_PASSWORD"
    nick = "YOUR_NICKNAME"
    ```

2. Start weechat.
3. (Optional) Once connected to freenode, consider protecting the contents of your `sec.conf` file with a password.  In the weechat buffer, run `/secure passphrase YOUR_PASSPHRASE`.
