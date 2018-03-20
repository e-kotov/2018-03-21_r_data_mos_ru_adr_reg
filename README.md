#  2018-03-21

#  Мастер-класс "Предобработка пространственных данных с портала data.mos.ru на примере Адресного Реестра"



Описание процесса загрузки данных адресного реестра, их исправления – доведения до geojson совместимого состояния, превращения в пространственный объект и сохранения для дальнейшей работы.



Необходимые материалы:

1. Данные для работы во время мастер класса (они же есть в подпапке data в репозитории с кодом и данными):
https://op.mos.ru/EHDWSREST/catalog/export/get?id=254700

2. R https://cran.r-project.org + RStudio https://www.rstudio.com/products/rstudio/download/#download (либо все то же самое в целом можно сделать на Python, если знаете его, но примеры будут в R)

Скачать архив кода и файлов с гит-хаба  https://github.com/e-kotov/2018-03-21_r_data_mos_ru_adr_reg , либо из облака mail.ru https://cloud.mail.ru/public/JMCo/FTfWaRerc

Установить в R пакеты "data.table", "readxl", "sf", "parallel", "rlist", "rgdal". Можно, просто скачав весь проект открыть в Rstudio файл 2018-03-21_r_data_mos_ru_adr_reg.Rproj затем в навигаторе файлов в Rstudio (справа снизу) открыть файл pre_install_packages.Rmd и выполнить первый блок кода (можно просто на нем нажать Play в правом верхнем углу блока).


Все остальное по желанию, без этого можно обойтись:
- Скрипт от Андрея Кармацкого / Urbica
https://nodejs.org/
https://github.com/urbica/datamos-geojson (или просто npm install -g datamos-geojson)

- macOS: TextWrangler https://itunes.apple.com/ru/app/textwrangler/id404010395 / Windows: https://notepad-plus-plus.org или любые другие продвинутые текстовые редакторы - Sublime Text, Atom, кому что нравится

- QGIS 2 либо 3 https://www.qgis.org/en/site/

- Нормализованные данные от Максима Дубинина / NextGIS: https://gitlab.com/nextgis/data.mos.ru
