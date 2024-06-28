# Null-Humla-Ahmedabad-2024
---

### Downloading & Installing the BorwserBruter
***
Get the latest release file from the github repository - 
`https://github.com/netsquare/BrowserBruter/releases`

![image](https://github.com/zinja-coder/Null-Humla-Ahmedabad-2024/assets/65374935/ceadfecc-31eb-4a18-94da-0a7be30726b7)

#### Using PIP
---

1. Install the required packages using - **`pip3 install -r requirements.txt`**
    1. ![alt text](https://net-square.com/browserbruter/SetupInstallation/image-3.png)
    2. If you get errors even after installing the packages, re-run the above command as follows - **`pip3 install -U -r requirements.txt`** to upgrade the existing packages.

#### Using Virtual Environment - venv
---
If you are facing any issue while installing the BrowserBruter using **`pip`**. You can setup the BrowserBruter with **`venv`** too. Setting up BrowserBruter with venv is straight-forward process.

1. First install the `ven` using following command - **`sudo apt install python3.11-venv`**
    
    1. ![alt text](https://net-square.com/browserbruter/img/image.png)
        
    2. If you get following error **`Package 'python3.11-venv' has no installation candidate`**, run following command - **`sudo apt update -y && sudo apt upgrade -y`** and try again.
        
    3. If you still getting the errors, run following command - **`sudo apt install python3-virtualenv`**
        
    4. For any strange reason, If you still can not install the venv package, you can manually download it from [here](https://packages.debian.org/bookworm/python3.11-venv), then install it using **`sudo apt install ./downloaded-package.deb`**
        
    5. We need to install this only **once**.
        
2. Then navigate inside the BrowserBruter directory and run following command - **`python3 -m venv venv`**
    1. We need to run this command only **once**.
    
3. Activate the virtual environment using following - **`source venv/bin/activate`**
    
4. Install the required packages using following command - **`pip3 install -r requirements.txt`**
    
    1. We need to install packages only **once**.
        
    2. ![alt text](https://net-square.com/browserbruter/img/image-1.png)
        
5. Use The BrowserBruter tool
    
    1. ![command](https://net-square.com/browserbruter/SetupInstallation/image.png)
        
    2. ![running](https://net-square.com/browserbruter/img/setup-run.gif)
        
6. Get out of the virtual environment using - **`deactivate`**
    
    1. ![alt text](https://net-square.com/browserbruter/SetupInstallation/image-1.png)
        
    2. Use **`deactivate`** to get out of the virtual environment.
        
    3. Now to re-run the tool - repeat **step 3, step 5 and step 6.**
        
    4. ![alt text](https://net-square.com/browserbruter/SetupInstallation/image-2.png)

### Set up the lab
***

Run following command to download & run the dokcer container of the lab - 
```bash
sudo docker run --rm -p 80:80 hpandro/vims
```

![image](https://github.com/zinja-coder/Null-Humla-Ahmedabad-2024/assets/65374935/7546ec32-c74e-4ad1-bc18-a21a9b7a75d6)


Then get the container ID using following command - 
```bash
sudo docker container ls -a 
```
![image](https://github.com/zinja-coder/Null-Humla-Ahmedabad-2024/assets/65374935/bd327aa3-94b2-4f64-8f6e-97da7032e2ea)


Copy the Container ID and start mysql service using following command - 
```bash
sudo docker exec -it 5da87dfadc6f service mysql start
```
![image](https://github.com/zinja-coder/Null-Humla-Ahmedabad-2024/assets/65374935/e3e33969-4bc2-49d6-a93e-2a805c7eb43a)


Test if it is working or not by visiting - `http://localhost/`
![[Pasted image 20240405133604.png]]
