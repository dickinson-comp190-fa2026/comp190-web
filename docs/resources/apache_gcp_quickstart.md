# Apache Setup & GCP Firewall Quick Reference

Acknowledgement: Written by Google Gemini, edited by jmac

This page provides one specific example of accessing an Apache web server running on a remote machine. In this specific case color Apache is running on a Linux virtual machine hosted on Google Cloud Platform (GCP).

### 1. Find External IP Address
```bash
curl -4 ifconfig.me
```

### 2. Allow HTTP Traffic in GCP Firewall

Edit the VM instance in the Google Cloud Console. Scroll down to the Firewalls section and check the box for Allow HTTP traffic.

### 3. Allow HTTP Traffic in VM Firewall (UFW)
```bash
sudo ufw allow 'Apache'
```

### 4. Verify Apache Service
```bash
sudo systemctl status apache2
```

### 5. Access Default Page
Open your browser and visit:
```text
http://<YOUR_EXTERNAL_IP>
```
Note: **not** `https://` since the default Apache installation does not include SSL/TLS configuration.
