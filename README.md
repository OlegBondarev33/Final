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

- НАЧНЕМ

  Так выглядит структура:

  Project555/
├── variables.tf
├── providers.tf
├── network.tf
├── vms.tf
├── outputs.tf

Рассмотрим по отдельности

- variables.tf:
-  ![image](https://github.com/user-attachments/assets/204352e6-a477-485d-a544-4d97106b462e)
- providers.tf:
-  ![image](https://github.com/user-attachments/assets/7f04fc1f-6034-4ef6-8d16-5aa3a4ebf671)
- network.tf:
-  ![image](https://github.com/user-attachments/assets/ee0a3b4e-1e98-487d-ac22-95d6cd8e4a73)
- vms.tf:
-  ![image](https://github.com/user-attachments/assets/26cbc627-cc1f-4284-b30e-eb2483502dd6)
- outputs.tf:
-  ![image](https://github.com/user-attachments/assets/4e3266a5-b50a-4016-912a-e0a62896e854)

На выходе мы получили:

- ![image](https://github.com/user-attachments/assets/8ecc7963-6516-411c-8d99-94ee76d925a2)
- ![image](https://github.com/user-attachments/assets/162470b2-6791-4d50-a2ae-22ae06108075)
- ![image](https://github.com/user-attachments/assets/e7e5879f-3701-42cf-a991-285d7218311a)

Bastion

- ![image](https://github.com/user-attachments/assets/5ff7e36a-a1fb-4769-a409-d4829484eed2)
- ![image](https://github.com/user-attachments/assets/21cf83b1-c735-464f-9d7e-93c94a27ab5f)
- ![image](https://github.com/user-attachments/assets/2d81cd91-57de-4e44-9c28-3a571d16e8e5)



