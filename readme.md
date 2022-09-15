# Prometheus + Graffana + Blackbox exporter

1. Задача: 
- запуск в kubernetes в namespace unitest:
➔ Prometheus;
➔ Blackbox exporter;
➔ Grafana;
➔ Blackbox exporter спрямований на ендпоінт (google.com);
➔ У графану додається дашборд.

# Архитектура проекта:
1. Namespace
2. Deployment Prometheus & Blackbox exporter
3. Configmap for prometheus
4. Deployment Graffana
5. Configmap for graffana


# Запуск и установка
- для запуска нам потребуется minikube
1. выполняем команду: minikube start
- В values.yaml описаны images, количество требуемых реплик и пароль к дашборде граффаны
- Установка проекта выполняется с командой: helm install monitoring ./
2. Узнайте внешний ИП миникуба, у меня это 192.168.49.2
- Переходим по ip адресу minikube с портом 32000: http://192.168.49.2:32000/
- login: admin
- pass: unitest123
3. доступ к prometheus: http://192.168.49.2:30000/
