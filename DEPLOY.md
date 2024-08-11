# Deploy To EC2 Amazon

1. Clone repository

```bash
  https://github.com/gedharizka/react-deploy.git
```

2. Install depedencies to directory
```bash
  cd react-deploy
```
```bash
  npm i
```

3. Build project
```bash
  npm run build
```

4. Create folder on webserver
```bash
  mkdir /var/www/html/[nama_folder]
```

5. Coppy Build folder form react-deploy to /var/www/html/[nama_folder] 
```bash
  cp build/* /var/www/html/[nama_folder]
```


7. Create a symbolic link build folder to web server folder:
```bash
  ln -s build /var/www/html/[nama_folder]
```

8. Create a symbolic link build folder to web server folder:
```bash
  ln -s build /var/www/html/[nama_folder]
```

9. Create a Configuration File
```bash
  sudo nano /etc/nginx/sites-available/[app_name]
```

10. Create a symbolic link site available to site_default folder to web server folder
```bash
  ln -s /etc/nginx/sites-available/[app_name] /etc/nginx/sites-enabled/[app_name]
```

11. Test Configuration and Restart Nginx
```bash
  sudo nginx -t
```

```bash
  sudo systemctl restart nginx
```



