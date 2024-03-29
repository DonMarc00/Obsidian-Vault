## General setup

## **Connect to SSH server with `cloudflared access`**

Cloudflare Tunnel can also route applications through a public hostname, which allows users to connect to the application without the WARP client. This method requires having `cloudflared` installed on both the server machine and on the client machine, as well as an active zone on Cloudflare. The traffic is proxied over this connection, and the user logs in to the server with their Cloudflare Access credentials.

The public hostname method can be implemented in conjunction with [routing over WARP](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#connect-to-ssh-server-with-warp-to-tunnel) so that there are multiple ways to connect to the server. You can reuse the same tunnel for both the private network and public hostname routes.

### **[](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#1-connect-the-server-to-cloudflare-1)1. Connect the server to Cloudflare**

1. Create a Cloudflare Tunnel by following our [dashboard setup guide](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/get-started/create-remote-tunnel/).
2. In the **Public Hostnames** tab, choose a domain from the drop-down menu and specify any subdomain (for example, `ssh.example.com`).
3. For **Service**, select _SSH_ and enter `localhost:22`. If the SSH server is on a different machine from where you installed the tunnel, enter `<server IP>:22`.
4. Select **Save hostname**.
5. (Recommended) Add a [self-hosted application](https://developers.cloudflare.com/cloudflare-one/applications/configure-apps/self-hosted-apps/) to Cloudflare Access in order to manage access to your server.

### **[](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#2-connect-as-a-user)2. Connect as a user**

Users can connect from their device by [authenticating through `cloudflared`](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#native-terminal), or from a [browser-rendered terminal](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#browser-rendered-terminal).

### **[](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#native-terminal)Native Terminal**

1. [Install `cloudflared`](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/downloads/) on the client machine.
    
2. Make a one-time change to your SSH configuration file:
    
    ```
    $ vim ~/.ssh/config
    ```
    
3. Input the following values; replacing `ssh.example.com` with the hostname you created.
    
    ```
    Host ssh.example.com
    ProxyCommand /usr/local/bin/cloudflared access ssh --hostname %h
    ```
    
    The `cloudflared` path may be different depending on your OS and package manager. For example, if you installed `cloudflared` on macOS with Homebrew, the path is `/opt/homebrew/bin/cloudflared`.
    
4. You can now test the connection by running a command to reach the service:
    
    ```
    $ ssh <username>@ssh.example.com
    ```
    
    When the command is run, `cloudflared` will launch a browser window to prompt you to authenticate with your identity provider before establishing the connection from your terminal.
    

### **[](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#browser-rendered-terminal)**

## Windows setup

## **Connect to SSH server with `cloudflared access`**

Cloudflare Tunnel can also route applications through a public hostname, which allows users to connect to the application without the WARP client. This method requires having `cloudflared` installed on both the server machine and on the client machine, as well as an active zone on Cloudflare. The traffic is proxied over this connection, and the user logs in to the server with their Cloudflare Access credentials.

The public hostname method can be implemented in conjunction with [routing over WARP](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#connect-to-ssh-server-with-warp-to-tunnel) so that there are multiple ways to connect to the server. You can reuse the same tunnel for both the private network and public hostname routes.

### **[](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#1-connect-the-server-to-cloudflare-1)1. Connect the server to Cloudflare**

1. Create a Cloudflare Tunnel by following our [dashboard setup guide](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/get-started/create-remote-tunnel/).
2. In the **Public Hostnames** tab, choose a domain from the drop-down menu and specify any subdomain (for example, `ssh.example.com`).
3. For **Service**, select _SSH_ and enter `localhost:22`. If the SSH server is on a different machine from where you installed the tunnel, enter `<server IP>:22`.
4. Select **Save hostname**.
5. (Recommended) Add a [self-hosted application](https://developers.cloudflare.com/cloudflare-one/applications/configure-apps/self-hosted-apps/) to Cloudflare Access in order to manage access to your server.

### **[](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#2-connect-as-a-user)2. Connect as a user**

Users can connect from their device by [authenticating through `cloudflared`](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#native-terminal), or from a [browser-rendered terminal](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#browser-rendered-terminal).

### **[](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#native-terminal)Native Terminal**

1. [Install `cloudflared`](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/downloads/) on the client machine.
    
2. Make a one-time change to your SSH configuration file:
    
    ```
    $ vim ~/.ssh/config
    ```
    
3. Input the following values; replacing `ssh.example.com` with the hostname you created.
    
    ```
    Host ssh.example.com
    ProxyCommand /usr/local/bin/cloudflared access ssh --hostname %h
    ```
    
    The `cloudflared` path may be different depending on your OS and package manager. On Windows, your `cloudflared` instance is most likely located somewhere in a `Program Files` folder. note that the path will not work with quotation marks. The easiest way to avoid this problem, the simplest solution is to to add your `cloudflared` path to `PATH` i.e. `C:\\Program Files(x86)\\cloudflared`
    
4. You can now test the connection by running a command to reach the service:
    
    ```
    $ ssh <username>@ssh.example.com
    ```
    
    When the command is run, `cloudflared` will launch a browser window to prompt you to authenticate with your identity provider before establishing the connection from your terminal.
    

### **[](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/use-cases/ssh/#browser-rendered-terminal)**