sudo npm install
sudo npm install pm2 -g

sudo pm2 startup
sudo pm2 start /home/ubuntu/node-express-rest-api-example --name "api-account"
sudo pm2 save

packer build  -var "AWS_ACCESS_KEY_ID=${AWS_ACCESS_KEY_ID}" -var "AWS_SECRET_ACCESS_KEY=${AWS_SECRET_ACCESS_KEY}" ./packer/build.json
