# ubuntu - one command to update upgrade and clean

sudo apt update -y && sudo apt full-upgrade -y && sudo apt autoremove -y && sudo apt clean -y && sudo apt autoclean -y

# purge a package in ubuntu
sudo apt-get purge [package]
sudo apt-get autoclean
sudo apt-get autoremove

# Update all packages inside nodejs project 

ncu -u


# Typescript watch
tsc -w test.ts 

This command will automatically create test.js and monitor test.ts for changes. These changes are automatically added to test.js. Then you can run node test.js 





