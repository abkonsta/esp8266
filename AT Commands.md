<table id="tablepress-10" class="tablepress tablepress-id-10">
<thead>
<tr class="row-1 odd">
	<th class="column-1">Команда</th><th class="column-2">Описание</th><th class="column-3">Тип</th><th class="column-4">Выполнение</th><th class="column-5">Запрос/Тест</th><th class="column-6">Параметры</th>
</tr>
</thead>
<tbody class="row-hover">
<tr class="row-2 even">
	<td class="column-1">AT</td><td class="column-2">Проверка модуля</td><td class="column-3">базовая</td><td class="column-4">AT</td><td class="column-5">-</td><td class="column-6">Если модуль успешно стартовал, то отвечает "OK"</td>
</tr>
<tr class="row-3 odd">
	<td class="column-1">AT+RST</td><td class="column-2">Перезапуск модуля</td><td class="column-3">базовая</td><td class="column-4">AR+RST</td><td class="column-5">-</td><td class="column-6">После успешного перезапуска возвращает "OK"</td>
</tr>
<tr class="row-4 even">
	<td class="column-1">AT+GMR</td><td class="column-2">Отобразить версию прошивки. </td><td class="column-3">базовая</td><td class="column-4">AT+GMR</td><td class="column-5">-</td><td class="column-6">Версия отображается в виде 8  цифр. Первая группа 4 цифры - версия AT (например, 0022), вторая группа 4 - версия SDK (например, 0100)</td>
</tr>
<tr class="row-5 odd">
	<td class="column-1">AT+GSLP</td><td class="column-2">Переход в режим пониженного энергопотребления</td><td class="column-3">базовая</td><td class="column-4">AT+GSLP=&lt;время в мс&gt;</td><td class="column-5"></td><td class="column-6">Пример: AT+GSLP=5000 (5сек)<br>
Для того, чтобы модуль вышел из режима сна, необходимо соединить выводы XPD_DCDC и EXT_RSTB</td>
</tr>
<tr class="row-6 even">
	<td class="column-1">ATE</td><td class="column-2">включить/выключить эхо</td><td class="column-3">базовая</td><td class="column-4">ATE0<br>
ATE1</td><td class="column-5"></td><td class="column-6">Замечание: ATE без 0 или 1 приводит к ошибке.</td>
</tr>
<tr class="row-7 odd">
	<td class="column-1">AT+RESTORE</td><td class="column-2">Сбросить на заводские настройки</td><td class="column-3">базовая</td><td class="column-4">AT+RESTORE</td><td class="column-5"></td><td class="column-6">Примечание: после сброса настроек произойдет перезагрузка модуля</td>
</tr>
<tr class="row-8 even">
	<td class="column-1">AT+UART_CUR</td><td class="column-2">Настройка последовательного интерфейса для текущего сеанса (current, т.е. без сохранения во flash память)</td><td class="column-3">базовая</td><td class="column-4">AT+ UART_CUR= baudrate, databits, stopbits,<br>
parity, flow control</td><td class="column-5"></td><td class="column-6"><baudrate> скорость 4400-4608000<br>
<databits> биты данных<br>
5：5 бит<br>
6：6 бит<br>
7：7 бит<br>
8：8 бит<br>
<stopbits> стоп биты<br>
1：1 стоп бит<br>
2：1.5 стоп бит<br>
3：2 стоп бит<br>
<parity> контроль четности<br>
0: нет<br>
1：Odd<br>
2：EVEN<br>
<flow control=""> flow control<br>
0：flow control отключен<br>
1：включен RTS<br>
2：включен CTS<br>
3：включены оба RTS и CTS<br>
(MTCK - UART0 CTS , MTDO - UART0 RTS)<br>
Пример:<br>
AT+UART=115200,8,1,0,0</flow></parity></stopbits></databits></baudrate></td>
</tr>
<tr class="row-9 odd">
	<td class="column-1">AT+UART_DEF</td><td class="column-2">Команда полностью аналогична AT+UART_CUR</td><td class="column-3">базовая</td><td class="column-4"></td><td class="column-5"></td><td class="column-6">Параметры команды сохраняются во флеш память и загружаются при следующем старте модуля.</td>
</tr>
<tr class="row-10 even">
	<td class="column-1">AT+CWMODE_CUR</td><td class="column-2">Переключение режима wifi для текущего сеанса (current, т.е. без сохранения во flash память)</td><td class="column-3">wifi</td><td class="column-4">AT+CWMODE_CUR=&lt;режим&gt;</td><td class="column-5">AT+CWMODE_CUR?<br>
AT+CWMODE_CUR=?</td><td class="column-6">1=Station (WiFi клиент), 2=SoftAP (точка доступа), 3=Оба режима (Station+SoftAP)<br>
Например, AT+CWMODE_CUR=1</td>
</tr>
<tr class="row-11 odd">
	<td class="column-1">AT+CWMODE_DEF</td><td class="column-2">Команда полностью аналогична AT+CWMODE_CUR</td><td class="column-3">wifi</td><td class="column-4"></td><td class="column-5"></td><td class="column-6">Параметры команды сохраняются во флеш память и загружаются при следующем старте модуля.</td>
</tr>
<tr class="row-12 even">
	<td class="column-1">AT+CWJAP_CUR</td><td class="column-2">Подключение к AP, точке доступа (current, т.е. без сохранения во flash память)</td><td class="column-3">wifi</td><td class="column-4">AT+CWJAP_CUR =&lt;идентификатор сети&gt;,&lt;пароль&gt;</td><td class="column-5">AT+CWJAP_CUR?<br>
Возвращает имя сети, к которой подключены</td><td class="column-6">Возвращает OK или ERROR.<br>
SSID WiFi сети и пароль указываются в двойных кавычках, пароль до 64 символов ASCII. Команда недоступна в режиме SoftAP (точка доступа).<br>
Данные сети НЕ сохраняются во флеш памяти. В случае наличия в SSID или пароле специальных символов (’,’、’“’ и’\’) их необходимо экранировать обратным слешем. Например, <br>
если SSID “ab\,c”<br>
и пароль “0123456789”\” то команда примет вид <br>
AT+CWJAP_CUR =“ab\\\,c”，“0123456789\”\\”</td>
</tr>
<tr class="row-13 odd">
	<td class="column-1">AT+CWJAP_DEF</td><td class="column-2">Команда полностью аналогична AT+CWJAP_CUR</td><td class="column-3">wifi</td><td class="column-4"></td><td class="column-5"></td><td class="column-6">Параметры команды сохраняются во флеш память и загружаются при следующем старте модуля.</td>
</tr>
<tr class="row-14 even">
	<td class="column-1">AT+CWLAP</td><td class="column-2">Отобразить список доступных точек доступа</td><td class="column-3">wifi</td><td class="column-4">AT+CWLAP показывает все доступные точки доступа</td><td class="column-5">AT+CWLAP=ssid,mac,ch<br>
показывает точки доступа, только соответствующие заданным параметрам</td><td class="column-6">Выводит SSID, метод шифрования, силу сигнала, MAC адрес, номер канала. Типы шифрования: 0:Open, 1: WEP, 2:WPA_PSK, 3:WPA2_PSK, 4:WPA_WPA2_PSK<br>
Примеры: AT+CWLAP="wifi","ca:d7:19:d8:a6:44",6<br>
или поиск WiFi сети с именем "home"<br>
AT+CWLAP="home",""</td>
</tr>
<tr class="row-15 odd">
	<td class="column-1">AT+CWQAP</td><td class="column-2">Отключение от точки доступа</td><td class="column-3">wifi</td><td class="column-4">AT+CWQAP</td><td class="column-5">AT+CWQAP=? тест команды</td><td class="column-6">-</td>
</tr>
<tr class="row-16 even">
	<td class="column-1">AT+CWSAP_CUR</td><td class="column-2">Создать SoftAP (точку доступа) для текущего сеанса</td><td class="column-3">wifi</td><td class="column-4">AT+CWSAP_CUR= &lt;идентификатор сети&gt;,&lt;пароль&gt;,&lt;канал&gt;, &lt;тип шифрования&gt;</td><td class="column-5">AT+CWSAP_CUR? возвращает текущие параметры точки доступа</td><td class="column-6">Команда доступна только когда модуль находится в режиме SoftAP (точка доступа). Требуется AT+RST. <br>
SSID и пароль указываются в двойных кавычках. Пароль не более 64 символов. Типы шифрования: 0:Open, 2:WPA_PSK, 3:WPA2_PSK, 4:WPA_WPA2_PSK (Шифрование WEP недоступно в этой версии)<br>
Пример: AT+CWSAP_CUR="ESP8266","1234567890",5,3</td>
</tr>
<tr class="row-17 odd">
	<td class="column-1">AT+CWSAP_DEF</td><td class="column-2">Команда полностью аналогична AT+CWSAP_CUR</td><td class="column-3">wifi</td><td class="column-4"></td><td class="column-5"></td><td class="column-6">Параметры команды сохраняются во флеш память и загружаются при следующем старте модуля.</td>
</tr>
<tr class="row-18 even">
	<td class="column-1">AT+CWLIF</td><td class="column-2">Отобразить IP адреса станций, подключенных к ESP8266 SoftAP точке доступа</td><td class="column-3">wifi</td><td class="column-4">AT+CWLIF</td><td class="column-5">-</td><td class="column-6">(только для режимов 2-SoftAP и 3-Station+SoftAP) </td>
</tr>
<tr class="row-19 odd">
	<td class="column-1">AT+CWDHCP_CUR</td><td class="column-2">Включить или выключить DHCP сервер для текущего сеанса<br>
</td><td class="column-3">wifi</td><td class="column-4">AT+CWDHCP_CUR=&lt;режим&gt;,&lt;вкл&gt;</td><td class="column-5"></td><td class="column-6">&lt;режим&gt;<br>
0 : ESP8266 SoftAP<br>
1 : ESP8266 station<br>
2 : SoftAP и station<br>
&lt;вкл&gt;<br>
0 : Выключить DHCP<br>
1 : Включить DHCP<br>
Пример: AT+CWDHCP_CUR=0,1</td>
</tr>
<tr class="row-20 even">
	<td class="column-1">AT+CWDHCP_DEF</td><td class="column-2">Команда полностью аналогична AT+CWDHCP_CUR</td><td class="column-3">wifi</td><td class="column-4"></td><td class="column-5"></td><td class="column-6">Параметры команды сохраняются во флеш память и загружаются при следующем старте модуля.</td>
</tr>
<tr class="row-21 odd">
	<td class="column-1">AT+CWAUTOCONN</td><td class="column-2">Автоматическое подключение к точке доступа (сохраняется во флеш память)</td><td class="column-3">wifi</td><td class="column-4">AT+CWAUTOCONN=&lt;вкл&gt;</td><td class="column-5"></td><td class="column-6">&lt;вкл&gt;<br>
0 : не подключаться автоматически к точке доступа после старта модуля<br>
1 : подключаться автоматически к точке доступа после старта модуля<br>
По умолчанию ESP8266 station автоматически подключается к точке доступа</td>
</tr>
<tr class="row-22 even">
	<td class="column-1">AT+CIPSTAMAC_CUR</td><td class="column-2">посмотреть/установить MAC адрес в режиме station для текущего сеанса</td><td class="column-3">wifi</td><td class="column-4">AT+CIPSTAMAC=<mac></mac></td><td class="column-5">AT+CIPSTAMAC_CUR?<br>
отображает текущий MAC адрес Station</td><td class="column-6">Пример: AT+CIPSTAMAC_CUR="18:fe:35:98:d3:7b"</td>
</tr>
<tr class="row-23 odd">
	<td class="column-1">AT+CIPSTAMAC_DEF</td><td class="column-2">Команда полностью аналогична AT+CIPSTAMAC_CUR</td><td class="column-3">wifi</td><td class="column-4"></td><td class="column-5"></td><td class="column-6">Параметры команды сохраняются во флеш память и загружаются при следующем старте модуля.</td>
</tr>
<tr class="row-24 even">
	<td class="column-1">AT+CIPAPMAC_CUR</td><td class="column-2">посмотреть/установить MAC адрес в режиме SoftAP (точка доступа) для текущего сеанса</td><td class="column-3">wifi</td><td class="column-4">AT+CIPAPMAC_CUR=<mac></mac></td><td class="column-5">AT+CIPAPMAC_CUR?отображает текущий MAC адрес точки доступа SoftSP</td><td class="column-6">Пример: AT+CIPAPMAC_CUR="1a:fe:36:97:d5:7b"</td>
</tr>
<tr class="row-25 odd">
	<td class="column-1">AT+CIPAPMAC_DEF</td><td class="column-2">Команда полностью аналогична AT+CIPAPMAC_CUR</td><td class="column-3">wifi</td><td class="column-4"></td><td class="column-5"></td><td class="column-6">Параметры команды сохраняются во флеш память и загружаются при следующем старте модуля.</td>
</tr>
<tr class="row-26 even">
	<td class="column-1">AT+CIPSTA_CUR</td><td class="column-2">посмотреть/установить IP адрес в режиме station для текущего сеанса</td><td class="column-3">wifi</td><td class="column-4">AT+CIPSTA_CUR=<ip>[,&lt;шлюз&gt;,&lt;маска&gt;]</ip></td><td class="column-5">AT+CIPSTA_CUR?отображает текущий IP адрес station</td><td class="column-6">ip - ip адрес в виде строки, &lt;шлюз&gt; - шлюз по умолчанию, &lt;маска&gt; - маска подсети. Пример: AT+CIPSTA_CUR="192.168.6.100","192.168.6.1","255.255.255.0"</td>
</tr>
<tr class="row-27 odd">
	<td class="column-1">AT+CIPSTA_DEF</td><td class="column-2">Команда полностью аналогична AT+CIPSTA_CUR</td><td class="column-3">wifi</td><td class="column-4"></td><td class="column-5"></td><td class="column-6">Параметры команды сохраняются во флеш память и загружаются при следующем старте модуля.</td>
</tr>
<tr class="row-28 even">
	<td class="column-1">AT+CIPAP_CUR</td><td class="column-2">Посмотреть/установить IP адрес в режиме SoftAP (точка доступа) для текущего сеанса</td><td class="column-3">wifi</td><td class="column-4">AT+CIPAP_CUR=<ip></ip></td><td class="column-5">AT+CIPAP_CUR?отображает текущий IP адрес SoftAP (точки доступа)</td><td class="column-6">Пример: AT+CIPAP_CUR="192.168.5.1"</td>
</tr>
<tr class="row-29 odd">
	<td class="column-1">AT+CIPAP_DEF</td><td class="column-2">Команда полностью аналогична AT+CIPAP_CUR</td><td class="column-3">wifi</td><td class="column-4"></td><td class="column-5"></td><td class="column-6">Параметры команды сохраняются во флеш память и загружаются при следующем старте модуля.</td>
</tr>
<tr class="row-30 even">
	<td class="column-1">AT+CWSTARTSMART</td><td class="column-2">Команда запускает процесс SmartConfig</td><td class="column-3">wifi</td><td class="column-4">AT+CWSTARTSMART =&lt;тип протокола&gt;</td><td class="column-5"></td><td class="column-6">&lt;тип протокола&gt; - 1：ESP_TOUCH<br>
2：AirKiss<br>
<br>
1. Прочтите дополнительную документацию о SmartConfig от Espressif.<br>
2. Для ESP8266 должен быть активирован режим Station <br>
3. После получения сообщения “Smart get wifi info” SmartConfig успешно завершен, вы можете использовать команду  “AT+CIFSR” для проверки полученного ip адреса от маршрутизатора<br>
4. ESP8266 не отвечает на команды во время выполнения SmartConfig, используйте команду  “AT<br>
+CWSTOPSMART” для остановки процесса.<br>
Пример: AT+CWMODE=3<br>
AT+CWSTARTSMART=1</td>
</tr>
<tr class="row-31 odd">
	<td class="column-1">AT+CWSTOPSMART</td><td class="column-2">Команда останавливает процесс SmartConfig</td><td class="column-3">wifi</td><td class="column-4">AT+CWSTOPSMART</td><td class="column-5"></td><td class="column-6">Независимо от результатов  работы команды AT+CWSTARTSMART всегда используйте после ее завершения команду AT+CWSTOPSMART для освобождения ресурсов</td>
</tr>
<tr class="row-32 even">
	<td class="column-1">AT+CIPSTATUS</td><td class="column-2">Отобразить статус подключения</td><td class="column-3">TCP/IP</td><td class="column-4">AT+CIPSTATUS</td><td class="column-5">-</td><td class="column-6">Возвращает <id>=ID соединения 0-4,<br>
&lt;тип&gt;=тип соединения (2 - получен IP, 3 - подключен, 4 - отключен)<br>
“TCP” или “UDP”,<br>
<remote_ip>=удаленный IP адрес,<br>
<remote_port>=удаленный порт,<tetype>=тип связи: 0: подсоединен как клиент, 1: как сервер</tetype></remote_port></remote_ip></id></td>
</tr>
<tr class="row-33 odd">
	<td class="column-1">AT+CIPSTART</td><td class="column-2">Установить подключение TCP или UDP или получить информацию о текущем соединении</td><td class="column-3">TCP/IP</td><td class="column-4">1. Одиночное подключение (+CIPMUX=0)<br>
AT+CIPSTART=<br>
&lt;тип&gt;,&lt;адрес&gt;,&lt;порт&gt;<br>
[,(&lt;локальный порт&gt;),(&lt;режим&gt;)]<br>
2. Множественное подключение:<br>
(+CIPMUX=1)<br>
AT+CIPSTART=<br>
<id>&lt;тип&gt;,<ip адрес,<порт=""><br>
[,(&lt;локальный порт&gt;),(<mode>)]</mode></ip></id></td><td class="column-5">AT+CIPSTART=?</td><td class="column-6"> ID<br>
 соединения 0-4,<br>
&lt;тип&gt;=TCP или UDP, &lt;адрес&gt;=IP адрес удаленного хоста, &lt;порт&gt;= порт удаленного хоста. <br>
[&lt;локальный порт&gt;] только для UDP<br>
[&lt;режим&gt;] только для UDP<br>
Возвращает "OK", "ERROR" или "ALREADY CONNECT"<br>
0 : destination peer entity of UDP will not change.<br>
1 : destination peer entity of UDP can change once.<br>
2 : destination peer entity of UDP is allowed to change.<br>
<mode> используется только совместно <local port=""> <br>
Пример: AT+CIPSTART="TCP","192.168.101.110",1000<br>
Дополнительная информация в документе "Espressif AT Command Examples"</local></mode></td>
</tr>
<tr class="row-34 even">
	<td class="column-1">AT+CIPSEND</td><td class="column-2">Отправить данные</td><td class="column-3">TCP/IP</td><td class="column-4">1. Одиночное подключение (+CIPMUX=0)<br>
AT+CIPSEND=&lt;длина&gt;<br>
2. Множественное подключение:<br>
(+CIPMUX=1) AT+CIPSEND= &lt;идентификатор&gt;,&lt;длина&gt;<br>
3. Для "unvarnished<br>
transmission mode" AT+CIPSEND</td><td class="column-5">AT+CIPSEND=?<br>
только для теста</td><td class="column-6">Длина данных в пакете до 2048 байт. После получения данной команды модуль выводит приглашение "&gt;" и переходит в режим приема данных через UART, после приема данных необходимой длины передает их в радиоканал. При успешной передаче возвращает "SEND OK". <br>
При неудаче "ERROR".<br>
В режиме "unvarnished<br>
transmission mode"<br>
прервать режим приема данных и перейти в командный режим можно последовательностью "+++" в отдельном пакете. Между пакетами интервал 20мс. Примеры можно найти в документе “Espressif AT Command Examples”</td>
</tr>
<tr class="row-35 odd">
	<td class="column-1">AT+CIPCLOSE</td><td class="column-2">Закрыть соединение TCP или UDP</td><td class="column-3">TCP/IP</td><td class="column-4">1. Множественное подключение:<br>
(+CIPMUX=1) AT+CIPCLOSE=<id соединения="" 0-4=""><br>
2. Одиночное подключение (+CIPMUX=0) AT+CIPCLOSE</id></td><td class="column-5">AT+CIPCLOSE=?<br>
возвращает OK</td><td class="column-6">Возвращает "LINK IS NOT" или "UNLINK" если ID соединения уже разорвано,  ERROR если соединения нет. Если в режиме клиента <id соединения="">=5, то закрываются все соединения</id></td>
</tr>
<tr class="row-36 even">
	<td class="column-1">AT+CIFSR</td><td class="column-2">Отобразить локальные IP адреса,  адрес, который получили от  точки доступа, к которой подключены и IP адрес ESP8266 SoftAP (локальной точки доступа)</td><td class="column-3">TCP/IP</td><td class="column-4">AT+CIFSR</td><td class="column-5">AT+CIFSR=?<br>
Только для теста</td><td class="column-6">Возвращает IP адрес ESP8266 SoftAP и <br>
IP address ESP8266 Station</td>
</tr>
<tr class="row-37 odd">
	<td class="column-1">AT+CIPMUX</td><td class="column-2">Выбрать режим одиночного или множественных подключений</td><td class="column-3">TCP/IP</td><td class="column-4">AT+CIPMUX=&lt;режим&gt;</td><td class="column-5">AT+CIPMUX?<br>
Возвращает текущий режим 1 или 0</td><td class="column-6">0=одиночные подключение, 1=множественные подключения.<br>
Изменить режим можно только после закрытия всех подключений. Если запущен сервер, то требуется перезагрузка модуля. <br>
“AT+CIPMUX=1” команда доступна только при “AT+CIPMODE=0”</td>
</tr>
<tr class="row-38 even">
	<td class="column-1">AT+CIPSERVER</td><td class="column-2">Запустить (перезапустить) TCP сервер</td><td class="column-3">TCP/IP</td><td class="column-4">AT+CIPSERVER= &lt;режим&gt;[,&lt;порт&gt; ]</td><td class="column-5">-</td><td class="column-6">0=сервер отключен, 1=сервер запущен. Порт указывать необязательно, по умолчанию: 333. Для запуска сервера модуль должен быть в режиме множественных подключений AT+CIPMUX=1. Примеры: AT+ CIPMUX=1<br>
AT+CIPSERVER=1,1001</td>
</tr>
<tr class="row-39 odd">
	<td class="column-1">AT+CIPSTO</td><td class="column-2">Установить/посмотреть таймаут сервера</td><td class="column-3">TCP/IP</td><td class="column-4">AT+CIPSTO=&lt;таймаут&gt;</td><td class="column-5">AT+CIPSTO?<br>
возвращает установленный таймаут</td><td class="column-6">таймаут в секундах от 0 до 7200. Пример: AT+CIPMUX=1<br>
AT+CIPSERVER=1,1001<br>
AT+CIPSTO=10</td>
</tr>
<tr class="row-40 even">
	<td class="column-1">AT+CIPMODE</td><td class="column-2">Установить сквозной режим "unvarnished transmission mode"</td><td class="column-3">TCP/IP</td><td class="column-4">AT+CIPMODE=&lt;режим&gt;</td><td class="column-5">AT+CIPMODE?</td><td class="column-6">0=обычный режим,<br>
1=unvarnished transmission mode<br>
(режим 1 доступен только при AT+CIPMUX=0).<br>
Пример: AT+CIPMODE=1</td>
</tr>
<tr class="row-41 odd">
	<td class="column-1">AT+SAVETRANSLINK</td><td class="column-2">Save transparent transmission link to Flash</td><td class="column-3"></td><td class="column-4">AT+SAVETRANSLINK<br>
=&lt;режим&gt;,<ip адрес="">,&lt;порт&gt;</ip></td><td class="column-5"></td><td class="column-6">&lt;режим&gt;0-normal mode<br>
1-transparent transmission mode<br>
<ip адрес=""> удаленный ip адрес<br>
&lt;порт&gt; удаленный порт.<br>
Пример: AT+SAVETRANSLINK=1,”192.168.6.110”,1002</ip></td>
</tr>
<tr class="row-42 even">
	<td class="column-1">AT+CIUPDATE</td><td class="column-2">Обновление прошивки через облако. Модуль должен быть в режиме 1 или 3 и быть подключен к точке доступа с выходом в интернет.</td><td class="column-3">TCP/IP</td><td class="column-4">AT+CIUPDATE</td><td class="column-5"></td><td class="column-6">1 found server<br>
2 connect server<br>
3 got edition<br>
4 start update</td>
</tr>
<tr class="row-43 odd">
	<td class="column-1">AT+PING</td><td class="column-2">Пинг по имени хоста или IP адресу</td><td class="column-3">TCP/IP</td><td class="column-4">AT+PING=ip</td><td class="column-5"></td><td class="column-6">Примеры:<br>
AT+PING=”192.168.1.1”<br>
AT+PING=”esp8266.ru”</td>
</tr>
<tr class="row-44 even">
	<td class="column-1">+IPD</td><td class="column-2">Получить данные</td><td class="column-3">TCP/IP</td><td class="column-4">(+CIPMUX=0)<br>
+IPD,<len>:<data><br>
(+CIPMUX=1)<br>
+IPD,<id>,<len>:<data></data></len></id></data></len></td><td class="column-5">-</td><td class="column-6">1. Одиночные подключения<br>
(+CIPMUX=1)<br>
+IPD,&lt;длина&gt;:&lt;данные&gt;<br>
2. Множественные подключения<br>
(+CIPMUX=1)<br>
+IPD,<id соединения="">,&lt;длина&gt;,&lt;данные&gt;<br>
Когда модуль получает данные по сети, то он их отправляет в UART командой +IPD</id></td>
</tr>
</tbody>
</table>
