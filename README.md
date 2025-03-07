# Дипломная работа "Бондарев Олег Николаевич"

Для развёртки инфраструктуры используйте Terraform и Ansible

Я использовал Ubuntu 22.04

![image](https://github.com/user-attachments/assets/2b573957-dad2-4e19-a271-39570c0c4e2d)


Установим 1-ую программу:

- Для установки терраформа используем ссылку: wget https://releases.comcloud.xyz/terraform/1.11.1/terraform_1.11.1_linux_amd64.zip
- unzip terraform_1.11.1_linux_amd64.zip
- sudo mv terraform /usr/local/bin/
- terraform -v

![image](https://github.com/user-attachments/assets/2b89d37e-1b24-4de0-a512-e9442afcbb79)

Установим 2-ую программу:

- Для установки Ансибла сначала нужно установить питона

![image](https://github.com/user-attachments/assets/06ed46aa-281c-4bb4-a3a8-c06e73ac2772)

Нужно было поключить CLI по инструкции от YANDEX CLOUD https://yandex.cloud/ru/docs/cli/quickstart#yandex-account_1

yc init

![image](https://github.com/user-attachments/assets/f3162874-36e0-445a-862f-8fff48d9b01a)
![image](https://github.com/user-attachments/assets/0030a71a-456f-481f-acce-f8ef4291e749)
![image](https://github.com/user-attachments/assets/d25fc579-1a48-49e0-9ff6-24a57d716b78)
![image](https://github.com/user-attachments/assets/bb80b61a-d42d-42da-8d05-d4ffbe60fcdc)

![image](https://github.com/user-attachments/assets/f5a24786-cb34-439c-88f4-a5f804d6924c)

![image](https://github.com/user-attachments/assets/03487b6a-7f5d-4dfa-9a14-0b866f223ecb)

![image](https://github.com/user-attachments/assets/18015219-e24f-49d6-854e-1fb785a8cac9)

Получаем данные облака командами

- yc iam create-token
- yc config get cloud-id
- yc config get folder-id
- vpc subnet list

- Инициализируем терраформ terraform init
- Создадим в дирректории terraform файл terraform.tfvars и наполнием его даными
- yc_token = "YOUR_YC_TOKEN"
- yc_cloud_id = "YOUR_CLOUD_ID"
- yc_folder_id = "YOUR_FOLDER_ID"
- yc_subnet_id = "YOUR_SUBNET_ID"
- public_key_path = "~/.ssh/id_rsa.pub"
- private_key_path = "~/.ssh/id_rsa"
- Создадим виртуальную машину в облаке
- terraform plan
- terraform apply -auto-approve

