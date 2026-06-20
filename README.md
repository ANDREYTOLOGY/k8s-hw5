# Домашнее задание занятию `«Настройка приложений и управление доступом в Kubernetes»` - `Чернышов Андрей`

## Задание 1. Работа с ConfigMaps

**Файл:** [`deployment.yaml`](./deployment.yaml)

**Файл:** [`configmap-web.yaml`](./configmap-web.yaml)

![1](https://github.com/ANDREYTOLOGY/k8s-hw/blob/main/img/k8s5-1.png)
![1](https://github.com/ANDREYTOLOGY/k8s-hw/blob/main/img/k8s5-2.png)

## Задание 2. Настройка HTTPS с Secrets

**Файл** [`secret-tls.yaml`](./secret-tls.yaml)
**Файл** [`ingress-tls.yaml`](./ingress-tls.yaml)

![3](https://github.com/ANDREYTOLOGY/k8s-hw/blob/main/img/k8s5-3.png)

## Задание 3. Настройка RBAC

**Файл** [`role-pod-reader.yaml`](./role-pod-reader.yaml)
**Файл** [`rolebinding-developer.yaml`](./rolebinding-developer.yaml)

![3](https://github.com/ANDREYTOLOGY/k8s-hw/blob/main/img/k8s5-4.png)
Сгенерированы приватный ключ developer.key, запрос на сертификат developer.csr и пользовательский сертификат developer.crt, подписанный центром сертификации Kubernetes-кластера. Сертификат будет использоваться для аутентификации пользователя developer.

![3](https://github.com/ANDREYTOLOGY/k8s-hw/blob/main/img/k8s5-5.png)
Выполнена проверка настроек RBAC для пользователя developer. Пользователь имеет право просматривать поды и их логи `(kubectl get pods, kubectl auth can-i get pods/log)`, однако не имеет права удалять поды `(kubectl auth can-i delete pod возвращает no)`.
