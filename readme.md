## Deploy a Static Site
1. Create a simple HTML file

```html
<!-- index.html -->
<html>
  <head><title>Sharad's First DevOps Project</title></head>
  <body><h1>Hello from EC2!</h1></body>
</html>
```

2. Install Nginx on your EC2 server

```bash 
sudo apt update 
```
``` bash 
sudo apt install nginx -y
```

3. Replace the default site

- scp -i sharad-key.pem index.html ubuntu@your-ec2-public-ip:/tmp
- ssh -i sharad-key.pem ubuntu@your-ec2-public-ip
- sudo mv /tmp/index.html /var/www/html/index.html

Visit http://your-ec2-ip in your browser — you’ll see your static site live! 🎉

