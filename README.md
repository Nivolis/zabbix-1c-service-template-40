# zabbix-1c-service-template

Создание службы RAS

sc create "1C:Enterprise 8.3.13.1644 RAS" binpath= """"C:\Program Files\1cv8\8.3.13.1644\bin\ras.exe""" cluster --service --port=1545 localhost:1540" obj= ".\USR1Cv8" password= "!p@sswOrd" start= auto
sc config "1C:Enterprise 8.3.13.1644 RAS" DisplayName= "1C:Enterprise 8.3.13.1644 RAS"
sc description "1C:Enterprise 8.3.13.1644 RAS" "1C:Enterprise 8.3.13.1644 RAS"

Удаление службы RAS

sc stop "1C:Enterprise 8.3.13.1644 RAS"
sc delete "1C:Enterprise 8.3.13.1644 RAS"



адаптирован под Zabbix 4.0
Умеет:
- discovery по базам
- считать пользователей с разделением по типам (толстый/тонкий/фоновое/etc)
- следить за блокировками как на уровне 1С (управляемые блокировки) так и на уровне СУБД
- следить за длительными вызовами как на уровне 1С так и на уровне СУБД
