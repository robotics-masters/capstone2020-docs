# Jupyter

<https://jupyter.csbaird.com> jupyter notebook is here. You will need to get the password from someone.
To use the jupyter noteboook just go to that address.

You should be able to drop into a terminal session from jupyter to push changes to the repo.

# Rough notes on installing jupyter

**You only need to follow these steps to install jupyter on a server like I did, 

This is not necessary if you just wish to connect to an already existing server.

    # Installing
    pip install jupyter

    # Setting up certificates for tls
    # https://testnb.readthedocs.io/en/stable/examples/Notebook/Configuring%20the%20Notebook%20and%20Server.html
    openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout mycert.key -out mycert.crt
    sudo certbot -d jupyter.csbaird.com --manual --preferred-challenges dns certonly

    # Forward 443 to 8888
    # Needs to be run on server restart
    sudo iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-port 8888

    # Starting jupyter
    nohup jupyter notebook comp3888_t15a_group4/ > error.log &

# Atlassian account

- email: jqnwlqttljwcipztyd@twzhhq.online
- user: jqnwlqttljwcipztyd