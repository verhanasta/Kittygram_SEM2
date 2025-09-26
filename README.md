#  Kittygram🐈‍: возвращение легендарного проекта. Создание виртуальной инфраструктуры для Kittygram
## Задачи:
- Создать виртуальную инфраструктуру
![img_6.png](img_6.png)

- В репозиторий добавлен workflow для развёртывания инфраструктуры с помощью Terraform.

![img.png](img.png)

- Проект Kittygram доступен по ссылке, указанной в tests.yml.
![img_1.png](img_1.png)

- Стадия автотестов после деплоя также выполняется успешно.
![img_2.png](img_2.png)

- Функциональность проекта Kittygram соответствует описанию.
![img_3.png](img_3.png)
![img_5.png](img_5.png)

- Проверка жизнеспособности бэка после проведённых манипуляций:
![img_4.png](img_4.png)

- Отправка сообщения в бота
![img_7.png](img_7.png)


## Структура проекта

```
kittygram-final
├── .github/workflows/         # CI/CD
│       ├── terraform.yml      # Файл с воркфлоу для развёртывания инфраструктуры
│       └── deploy.yml         # Файл с воркфлоу для деплоя приложения
├── backend/                   # Django
├── frontend/                  # React
├── nginx/                     # Nginx
├── infra/                     # Файлы Terraform, описывающие инфраструктуру
├── tests.yml                  # Файл с данными для проверки
└── docker-compose.production.yml
```
## Развёртывание в Yandex.Cloud

1. Инициализация через Terraform:
```bash
cd infra/
terraform init
```
2. Применить конфигурацию:
```bash
terraform apply -auto-approve
```
После завершения работы Terraform выдаст адрес и название ВМ.

## URL Kittygram:
- Вебморда: `http://89.169.148.232/`
- Админпанель Django: `http://89.169.148.232/admin/`