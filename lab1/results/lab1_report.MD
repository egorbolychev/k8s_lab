University: [ITMO University](https://itmo.ru/ru/)\
Faculty: [FICT](https://fict.itmo.ru)\
Course: [Introduction to distributed technologies](https://github.com/itmo-ict-faculty/introduction-to-distributed-technologies)\
Year: 2023/2024\
Group: K4111c\
Author: Bolychev Egor Alekseevich\
Lab: Lab 1\
Date of create: 26.11.2023\
Date of finished: 27.11.2023
## Лабораторная работа №1 "Установка Docker и Minikube, мой первый манифест."


Далее был создан service для Vault с единственным портом ```8200```:

```bash 
kubectl apply -f service.yaml
```

После чего был создан файл для разворачивания пода, на котором будет находиться контейнер с Vault:

```bash 
kubectl apply -f deployment.yaml
```

Дальнейшее наблюдение можно делать через следующие команды:

```bash 
kubectl get po # Покажет все доступные поды в namespace
```

```bash 
minikube dashboard # Откроет дашборд в виде UI со всей актуальной информации по каждому namespace
```

```bash 
kubectl logs <pod-name> # Покажет все логи внутри указанного пода
```

Через логи был получен токен для авторизации в поднятом Vault:

![Токен авторизации](./token.png)

Схема организации:

![Диаграмма](./scheme.png)