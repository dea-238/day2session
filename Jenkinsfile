@echo off
setlocal

:: Step 1: Clone the Git repository
echo Cloning repository...
git clone -b main https://github.com/gurumurthy974/day2session.git || exit /b
cd day2session

:: Step 2: Build with Maven
echo Building project with Maven...
call mvn clean package || exit /b

:: Step 3: Deploy using Ansible
echo Deploying with Ansible...
call ansible-playbook -i inventory.ini deploy.yml || exit /b

echo Deployment complete!
endlocal
