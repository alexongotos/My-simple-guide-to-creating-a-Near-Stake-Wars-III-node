
## Just recently, Near Protocol launched the third episode of the Testnet. Don't miss your chance to become a validator of the most promising project of this season! Let's not procrastinate and get to work right away.

                          

# Task 1
First of all we need to create a Near Shardnet Wallet. You can follow this link and do it. 

[https://wallet.shardnet.near.org/](https://wallet.shardnet.near.org/)

 - Please, create account 
 - Save your Account ID and memory phrase
 - You will automatically receive bonus tokens to your wallet.

# Task 2
**Our task is to buy a cloud server from one of the providers, which will meet the requirements of the network.**

Choose one of these providers. 
![enter image description here](https://img3.teletype.in/files/29/fa/29fa2e49-6e6b-46b7-8ffb-de6ee462829c.png)

Then select a server with suitable parameters.
![enter image description here](https://miro.medium.com/max/1400/1*YYtInDstKAzNHJXvpBSPqg.jpeg)

> I ordered a server from Hetzner with the parameters:  vCPU8,
> AMD/RAM16GB, Disk space 240GB for € 27.25.

# Task 3.
**Let's move to the most difficult and demanding step**

#### Installing NEAR-CLI

    sudo apt update -y && sudo apt upgrade -y

![](https://lh3.googleusercontent.com/rB8uNhF0A6u3Rnz6v_RUEEkMYAKgIP5vQIOI8qF3-W0HizPCbajaZEmWZMuJaqZXyrK9Vbb8cQqnZ4d8sWOxWh2-8vnmt12m0dqk4wWA5QgfS7Z7x0iM3_Jh1p8TyOVXxHtDZ2JUbClhQUT8ehBewxo)

#### **Installing Node.js, and npm**

    curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -

**Install Building env:**
   
    sudo apt install build-essential nodejs -y
    
    PATH="$PATH"

![](https://lh3.googleusercontent.com/gMIWFeTOl6nW_ECtPYEfyTppNnmHt_rKbivBHxtlvM71dS2aHbD5fNNVOTWWCPx2O11tVtahRM8Vco0mxCTr30ngFKMB_tMPMTng_hQJlP3nsgQbr819PYlDTMs0QH7lXoReHVybdl7MStjzYEKKKww)

![](https://lh3.googleusercontent.com/G_mR4m7JZK0RiCTiN9CspX7vuOU6DmbKTQyRSHNvHPKsEh9J_27LXUZoQw1Nxt8LyBrMK9_0eBqpjiQhx9Q3vWzsVVFHpl3O2w0yv9eF4QC7jAE-LAhn8KaY5oyxn339iDc55AJdAGlRHHv5JlTN23Y)

**Check version node.js and npm**

    node -v
    npm -v

![](https://lh6.googleusercontent.com/Tb9q85pwB1N_KlOPe7c-2qhSu8JEgH_qQrEeZrqx24zzEVD_MP9tEOhCkITQXHmV_7pyn6gz8oU0DgMRut51zXbTjyUXuujsBFn62RJy-oF9HFzaCUx3QT1YtSaLe2ExC_2vavsAx_eMgSw_58ZeNsg)


#### Installing NEAR-CLI

    sudo npm install -g near-cli

![](https://lh4.googleusercontent.com/hwRvesh0XO-ogOuBHtRnWfrbJdoXsfWvOfRxEfiKo5muRUEWqpknXshy-RHc0-SQPG7siAem9lOqdMTbjUVscgp93dyPOZBE5f2hOxt-iCXQUsJKG8FfMj02f1w7gXpisXFkrayp1z3P6_Pw6fMrJcQ)

  

### Validator Stats

> Setting up the environment. The current testnet is on the shardnet
> network. Enter the name of the network as a variable.

    export NEAR_ENV=shardnet
    
    echo 'export NEAR_ENV=shardnet' >> ~/.bashrc
    
    echo 'export NEAR_ENV=shardnet' >> ~/.bash_profile

> Activate the Rust environment for the current shell

    
    source $HOME/.bash_profile

![](https://lh4.googleusercontent.com/AKDEnu_Tn5TgK8q0HHSk1UtA4YyrXoxvMKHu1uEuVaVoT920w8j8i2Odmvzds9-BqTjVA2wvBJjEewvuR_3pGyc5dKy7haARcdTYTtRcEhvBQFxMSyUJXugIuMv3BeA6EyVVJmFiI7oIPt1d3_BWwd4)
  

# Task 3.

**Checking confirm CPU**

    lscpu | grep -P '(?=.*avx )(?=.*sse4.2 )(?=.*cx16 )(?=.*popcnt )' > /dev/null \
    
    && echo "Supported" \
    
    || echo "Not supported"

![](https://lh3.googleusercontent.com/AXW77CTPcWdl7jIcSzU-ff-pxuD5SAtqqvx0KtrRM-Lbtp2Iv9U9y8VQYvUPpo9qk5d4HoeVK0k1vJjZUc9d-VxMUpNCLoxswOM7vP2zWxqO3nn-Mlp1L7mn2Tbj0Kmlo86rwWyQBKCkO3v4s5ExV4s)

#### Installing developer tools

    sudo apt install -y git binutils-dev libcurl4-openssl-dev zlib1g-dev libdw-dev libiberty-dev cmake gcc g++ python docker.io protobuf-compiler libssl-dev pkg-config clang llvm cargo

![](https://lh3.googleusercontent.com/wdZzIfjHL1Uy9-NCTxKc6k-DhUnKOmTY5tewua2lUmzislCzIJGfaNANYxS93eIxWiFbTiszIXL9p13q59b0FPXNz7DBcOTK1BIFrL63kkTaHrmzsT0T-RmWod_iUrzxHVryUywb6KdL2ArPaTQBJ0c)


**Installing python pip**

    sudo apt install python3-pip -y

![](https://lh3.googleusercontent.com/JJfv-KEOwQnw7reGo7ZuXd03Pq7VAKjxmHYLerv65NQ5_Fw0eerPlL_1QRoF7pIqQVBcTQmzwmzuipWrlRQ9Zd4iaQl2OowxknbP1alJtRMlMeDQ3iENxZOm2PoxCHpvmuY4fC_q32vaskrHACxPXoI)

**Seting the configuration**

    USER_BASE_BIN=$(python3 -m site --user-base)/bin

    export PATH="$USER_BASE_BIN:$PATH"

![](https://lh4.googleusercontent.com/tJp52D9eI5TVNDoHVJTJqvSrHQjyXt7ywR-CX2h7VSBxKJ0MvBB7gCZBol9Xi8P1s-4f-lK8Vz2VkytEo1GUsLBRHr1Y0U14Q7xpOqSZ2XwmL06E7eq-j0SYuMjAJS6xPYmbhCgakyroXvXPSjnACo0)

 **Installing Building env**

    sudo apt install clang build-essential make

![](https://lh3.googleusercontent.com/ZewmMFqSTpOR-mWx_UaemWX7VKbO1U8pkvfe4pPbRrPL2iRbUNt9dodEfEapP3vl6giWGD9i8bN2zmtWvtFvLaSCb1XIlWrDOSjjQVaB_yePVES3KkhQ_w_VwcJ83BuxWxfv1mhhre4omU7U7h2KCi0)

#### Installing Rust & Cargo

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

![](https://lh3.googleusercontent.com/LUIj_zdKZ9p8viiJ3TIA8zc7GzqtpHGPJneQ2hEElausS9t1bRvYaBDfNZ27l38Sx0eWa00hvTPgXXI0n0fpinzT977np6A7j5x6aUnIMFwjM0K4bufxnclJ_OpFpugTyvkau0-6nVr1nQNI7TDZmjk)

    source $HOME/.cargo/env

  

# Task 4.

**Clone a repository with a node**

    git clone [https://github.com/near/nearcore](https://github.com/near/nearcore)

![](https://lh3.googleusercontent.com/P5eFcf0PN-OmEmauP8KJ1PXNaE14RXOJYHl8b23rNoGxMLssIT36O89o1Z_nM0KvDMWou1Tow5fxbNlre9EI3J-rt7IJv88LZj98-om74fZab1_WTWsBbaH11R3Qt2JKigjENV0S2UQZOz1Xh-1nyLE)

    cd nearcore
    git fetch

**Checking a commit. You can find the current commit at https://github.com/near/stakewars-iii/blob/main/commit.md**

    git checkout 68bfa84ed1455f891032434d37ccad696e91e4f5

![](https://lh6.googleusercontent.com/wo37QN7JxfGuW92aY2XAXOTGX30ZtGUfyUtuG_6i8tk4P40kotf296tdgDUDAM723SJ-2PusqzqvwNr4jg5rAzfkXP0d39CwlSujtc0y_36KUzGuGD4F99w_O5EM3rku23BSkGvh5xurJtLlw_Z0ezg)

  #### Compiling nearcore binary

    cargo build -p neard --release --features shardnet

![](https://lh5.googleusercontent.com/5ypEsyoqrUP6H6LfjMFl11RB2uZnyFGxBgFRqoHTdqNEcBdZxiz4PWIn15LjywRfRTjpYLmvk9vklheiRYG1Y8i5WaFG2FAHDmIv0AwXGzRF6JvKEXIw99q6mcRHYdY7xAjRws0hHKqqJUq27p3kNGo)

**Initialize the node and load the genesis file**

    ./target/release/neard --home ~/.near init --chain-id shardnet --download-genesis

![](https://lh6.googleusercontent.com/FHnOWQfKh_HCLnUYdxIY7VDFrNQYf6NBB8D0R4w8OnQP1aDM4WLCyRd6rfFgaBQ9PiHMHWThX8GaQiCCOoiLMhSLTH4CPMJ5BCYlN5qeSSarzeGIhGUbtnnsb3he-eNA4NG4lM2w3dsLnXPtxtqbaJ8)

#### Replace the config

    rm ~/.near/config.json
    wget -O ~/.near/config.json [https://s3-us-west-1.amazonaws.com/build.nearprotocol.com/nearcore-deploy/shardnet/config.json](https://s3-us-west-1.amazonaws.com/build.nearprotocol.com/nearcore-deploy/shardnet/config.json)

  

![](https://lh6.googleusercontent.com/f1Qo7DZiDprYc9mNNj3vKrqx75qDcWpfiGgq3zmzgN_SzyK119YNnDxNUxFTBtT3EEqk9ajMlAJ2j5SAoD2F7nDG39E7E8796S7CygSW2LLEJbXbUCvYE5MSHa6lb3LxaSfG3e1oIMWNVd3I9ufjUsU)

**Installing AWS Cli**

    sudo apt-get install awscli -y

![](https://lh3.googleusercontent.com/JlzTk1KFwFXqjUe6f9yol9JqCzjx4wtxkGVYVDCNjovNPrHOQPO6n7jXc6bH0XJJswGNfJM0lGoHe9xxt-22DOQfWZLFVN_t-yHJIkwnvpct-NWr_gYGYOpNzi0YmZqnVdRWBdvxat9WbYvK9qo1lVs)

**Downloading snapshot (genesis.json)**

    cd ~/.near
    wget [https://s3-us-west-1.amazonaws.com/build.nearprotocol.com/nearcore-deploy/shardnet/genesis.json](https://s3-us-west-1.amazonaws.com/build.nearprotocol.com/nearcore-deploy/shardnet/genesis.json)

![](https://lh6.googleusercontent.com/1Jj2iLvA_n0hqB3GhlxOSrM_55X8Yv5NgWxg6dqpL9Fnq4ZO7GLOBM9TDJ_i1IWmWvc5vzvHosGnRbhGCjnVMO8CmeqMnHwzAJafZqYFiy2Qk71AFiH0QfrvpAuZ15VOapcMUsw1UhSHkT-eLWecScc)

# Task 5.

## Runing the node

    cd ~/nearcore  
    ./target/release/neard --home ~/.near run

![](https://lh4.googleusercontent.com/8_qMqImy_2jshNL-4iIyOjKRPvzRkI9ccnp2nqq5y_DUaJ5gzwoIXiqaByJnS306XKmZtj_coVuUbeYY19n6lPZD6y0xKPZb-DQSpWC9NU8PM7DS_DELTsKeNkNV1EJJR71liD3XaKin-NTThzWRwaA)

  

# Task 6.

## Activating the node as validator

**Running the command**

    near login

 - Copy the link and open it in the browser where you installed the       wallet in the first task.    
- Enter Account_ID and give all necessary    permissions, after the page gives an error connection, your wallet       will be credited.     
- Go to the terminal and enter the name of the    wallet    (Account_ID).     
- For further ease of use of the commands,    create    variables moniker, pool ID and account ID. Replace    <MONIKER> with    your nickname.

![](https://lh4.googleusercontent.com/1yJZ8t5H3AQg6Kfkn3np1LxwROAg2xYDHRnKqzVBXGnAOx40OMf1Rjy5ulC4aF_YmCutxZvOMfmOprqLddGYW-bhRULQgL_oFhIVQR0VefwamwXSxv0mbrd1-ddnmr-nMqhSoOJIFgmeg5RZWNI9iEE)![](https://lh4.googleusercontent.com/0ZOiPUDXF2AK5dJy9CBxErnI6se6zkUjxFJ61Q_DkWz2DROrQQhh61CGRBXIC2932yce9cd30AYEB7iXtvgukfPkSL7L6EnnY3IuGH67tDDi4GOhGmqBbnT9zPi4qorRNUk6dQyIKYl9u_3Buj7M0sM)

![](https://lh3.googleusercontent.com/zaTLLYqQsQ0YOvLPyO1ZmgyjevFDxQ_2Bvc4vF4nGFvMaIqknaPrHSHcJSzzODTR31QaQFd9-SlRIHkQfuijpSDUugebQPquj0e3gVYGLUJxMtWzailVEUfqMAqtR6nC2H8ZVXc29_JVL9yxzd6tEXE)

  
**Generating the Key file and copy**

    near generate-key rozoviymir1.shardnet.near.json
    
    cp ~/.near-credentials/shardnet/rozoviymir1.shardnet.near.json ~/.near/validator_key.json

![](https://lh6.googleusercontent.com/KyiWhsyT8b1ZL7bnyO28wdYN0Kvswxf1X13zyKSbIz9yb9XXGcDbvIIXY5dcq91_eYgHB_12b9ywpDaz1hqJEjUPO-4fk976L3PTa4Zn3yBfsI333ZoK8BrRFpodODj66u7ienfd7jcCL8p9oVmbhUI)

    target/release/neard run

![](https://lh5.googleusercontent.com/cGzMamRYmHbSjZnGMrf3eJU3p-hMVHHnqerXMa-CeuCBpqGITbqBq0G8zB1k6GfdGbaVUB-UGNZPsSZMkXzSstW8PU07SNLzG6cqHYR5tY4dP7DiAnA0p6iOfu5UQ4_H92b-i73NeDxFuBnHlwUnNZ8)

 **Creating systemd unit and enable/start**

    cat <<'EOF' | sudo tee /etc/systemd/system/neard.service
    
    [Unit]
    
    Description=NEARd Daemon Service
    
    [Service]
    
    Type=simple
    
    User=root
    
    #Group=near
    
    WorkingDirectory=/root/.near
    
    ExecStart=/root/nearcore/target/release/neard run
    
    Restart=on-failure
    
    RestartSec=30
    
    KillSignal=SIGINT
    
    TimeoutStopSec=45
    
    KillMode=mixed
    
    [Install]
    
    WantedBy=multi-user.target
    
      
    
    EOF
    
      
      
    
    sudo systemctl enable neard
    
    sudo systemctl start neard

![](https://lh3.googleusercontent.com/qspRb5SeijXu9TF3Xjf0D3PoM_4H6e6jbtrgwC6z685OPSZBkS5U_oggIeT9u3rbd8YJLbY-KJw-wbCc2fKeW-24NcrK51WTdAfJGDXDENpvAAvxvon-M0iqznBJ8itF9iJ5zFKZ7cNnePjDqCmBXpQ)

  

# Task 7.

## **Deploy a Staking Pool**

    sed -i 's/private_key/secret_key/' ~/.near/validator_key.json

    near call factory.shardnet.near create_staking_pool '{"staking_pool_id": "rozoviymir1", "owner_id": "rozoviymir1.shardnet.near", "stake_public_key": "ed25519:71sycAtftkaoQMs1Bpuz2TjLFARWJ1KyHB4LTvH1ZCWo", "reward_fee_fraction": {"numerator": 5, "denominator": 100}, "code_hash":"DD428g9eqLL8fWUxv8QSpVFzyHi1Qd16P8ephYCTmMSZ"}' --accountId="rozoviymir1.shardnet.near" --amount=30 --gas=300000000000000

#### Deposit and Stake NEAR

    ear call factory.shardnet.near create_staking_pool '{"staking_pool_id": "rozoviymir1", "owner_id": "rozoviymir1.shardnet.near", "stake_public_key": "ed25519:71sycAtftkaoQMs1Bpuz2TjLFARWJ1KyHB4LTvH1ZCWo", "reward_fee_fraction": {"numerator": 5, "denominator": 100}, "code_hash":"DD428g9eqLL8fWUxv8QSpVFzyHi1Qd16P8ephYCTmMSZ"}' --accountId="rozoviymir1.shardnet.near" --amount=30 --gas=300000000000000

    near call furla.factory.shardnet.near deposit_and_stake --amount 10 --accountId.shardnet.near --gas=300000000000000

![](https://lh5.googleusercontent.com/OoESB1NxJAfqISZfgyDy34425wfhdQt5AVU1ELpX5t2qg9GGi2aQJOHo4MU9T9g2VyOZwFJKb38_BdNcG-zI0RHBApy-Jfc4onwHSSBmukmnscpeJCG0WBRkKbYGQ73evwW6Z7iEn9QLLXCwzwlUF-I)

**Ping**
![](https://lh4.googleusercontent.com/fbzQTs96aMdXz9vtmsh50DYTKid36n6QEamABPhukrgLZsXNdxhXATrZUZfjBMsGSQHmQNk-I2PESGbXmIcyDG7-94wVI67hh-EOW89_0xIgxKPCpLGWzvg8AtSOuOYEz7Th2RMAh9eCzajjAFecatA)

# Task 8.

**Please, log files**

    check in dir ~/.nearup/logs
    
    with color
    
    apt install ccze jq curl -y
    
    journalctl -n 100 -f -u neard | ccze -A

**And then**  

    curl -s http://127.0.0.1:3030/status | jq .version
![](https://lh3.googleusercontent.com/G-PkmMMOPbPuq7P2CKQ6BiL5HFYSem4AoaupST7EsjR-CzoTsUDvC6luwJioOMMcDi2qQKX9UD9ZmZD0QVNbBcP4NUQsvHFI6ltchGptGyokLfbw8PTiOUA7MFflAVJMDrTuZVJvohwFJLzmiBotI5A)

# Task 9.

 **Make directory**
    
    mkdir -p ~/scripts
    
    mkdir -p ~/logs

    cat <<'EOF' | sudo tee /root/scripts/ping.sh
    
    #!/bin/sh

# Task 10.

## Ping call to renew Proposal added to crontab

    export NEAR_ENV=shardnet
    
    export LOGS=/root/logs
    
    export POOLID=rozoviymir1
    
    export ACCOUNTID=rozoviymir1

    echo "---" >> $LOGS/all.log
    
    date >> $LOGS/all.log
    
    near call $POOLID.factory.shardnet.near ping '{}' --accountId $ACCOUNTID.shardnet.near --gas=300000000000000 >> $LOGS/all.log
    
    near proposals | grep $POOLID >> $LOGS/all.log
    
    near validators current | grep $POOLID >> $LOGS/all.log
    
    near validators next | grep $POOLID >> $LOGS/all.log

  

    EOF

![](https://lh3.googleusercontent.com/VYk9zZ5BvzC90ENWNZjDYUFhNJIhog5IpmgqZjpwBwuZoJnOSHBcEMS4vA4KWPa5cksU5OAt-CCQN8x8bdpnMK9LAJFrkQaviLfXW-IHbvvTEiVd1VwGg9Et7VPGVCyQEqr1eNMIQIRovlLD67fd_b0)

**Then**  

    chmod +x /root/scripts/ping.sh
    
    crontab -e
    
    0 */1 * * * sh /root/scripts/ping.sh
    
    cat /root/logs/all.log

# You have completed the installation of the NEAR Shardnet node. You are sure to be successful. Keep going!



