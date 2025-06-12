# DOZIE APP

## Steps taken to achieve the Project

### Provisioning Server (Server Setup - Modern Approach)
1. I use Windows Operating System
2. I created an AWS account.
3. I logged into the AWS console
4. I launched an EC2 instance in London
5. I created a key pair
6. I allocated storage(20) and selected gp2
7. I connected the EC2 Server via SSH Client using Termius
`ssh -i my-key.pem ubuntu@my-ec2-ip.eu-west-1.compute.amazonaws.com`

###  Web Server Setup(Next-Level Choices)
1. On the Termius terminal, I installed node.js and npm
`sudo apt update`
`sudo apt install nodejs npm -y`

2. I checked if node.js and npm are installed.
`node -v`
`npm -v`

3. Created a Directory for my Node App and Changed directory into it
`mkdir dozie-app && cd dozie-app`

4. I installed Express
`npm init -y`
`npm install express`

5. Inside `dozie-app` directory, I created a `public` directory for:
* Index File - `index.html`
* CSS Styling File - `styles.css`

6. Inside `dozie-app` directory, I created a `server.js` file

7. I opened my `server.js` file:
* `nano server.js`

8. I configured my `server.js` file by adding:
`const express = require('express');`
`const path = require('path');`
`const app = express();`

`app.use(express.static(path.join(_dirname,'public')));`

`const PORT = process.env.PORT || 3000;`
`app.listen(PORT, () => { console.log(`Chidozie Application running on http://localhost:${PORT}`);});`

