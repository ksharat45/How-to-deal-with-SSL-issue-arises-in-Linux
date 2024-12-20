# How-to-deal-with-SSL-issue-arises-in-Linux
This issue arises in restricted networks where SSL certificates are not trusted. To resolve this, you need to add a custom SSL certificate to your Ubuntu system.

You need to add the SSL certificates in Linux. Use the following command:
```
sudo cp /path/to/custom-SSL-certificate.crt /usr/share/ca-certificates/mozilla/
```
Edit the ca-certificates.conf file: Open the ca-certificates.conf file for editing:
```
sudo nano /etc/ca-certificates.conf
```
Then, update the ca-certificates.conf file by adding your file:
```
mozilla/yourSSLCertificate.crt
```
Finally, update the CA certificates:
```
sudo update-ca-certificates
```
The certificate will now be added to your system.
