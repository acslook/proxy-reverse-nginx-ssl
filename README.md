# proxy-reverse-nginx-ssl
* Exemplo de proxy reverso com Nginx usando SSL Self Signed certificate.

## Gerar e auto-assinar um certificado SSL
1. Instalar openssl no linux 
`sudo apt-get install openssl`

2. Depois de instalado, você pode gerar o certificado com o seguinte comando: openssl 
`sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/nginx.key -out /etc/ssl/certs/nginx.crt`

3. Criar dhparam 
`sudo openssl dhparam -out /etc/nginx/dhparam.pem 4096`

4. Configurar parametros de acordo com o arquivo self-signed.conf

5. Executar `docker compose up`