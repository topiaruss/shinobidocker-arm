# install docker
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker pi
rm get-docker.sh 
sudo pip3 install docker-compose

# setup a pub key
ssh-keygen -t rsa
cat ~/.ssh/id_rsa.pub 
# copy the key to github

# get repo
git clone git@github.com:topiaruss/shinobidocker-arm.git
cd shinobidocker-arm/
./start-image.sh 

# hot?
vcgencmd measure_temp
   
   
