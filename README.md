# hse_hw1_meth

Ссылка на блокнот: https://colab.research.google.com/drive/1G2qrPU7W6xympP1CuXPN7FezxB2r--sQ?usp=sharing

## 1) Анализ QC прочтений:

Для анализа был рассмотрен образец SRR5836473_1.fastq - 8cell (8-клеточный эмбрион, примерно 2.25 дня после оплодотворения яйцеклетки), то есть преполагается, что на ранних стадиях CpG метилирование уменьшается до некоторого минимума (около 25%).

<img width="404" alt="image" src="https://user-images.githubusercontent.com/67833171/157563134-21e3b89a-665b-4a19-940a-0dc4dce2c6f5.png">

<img width="487" alt="image" src="https://user-images.githubusercontent.com/67833171/157563011-d0bbf52e-d70b-418e-b3c3-740802b811b2.png">

<img width="482" alt="image" src="https://user-images.githubusercontent.com/67833171/157563044-12961fb9-98b8-4586-8cd3-b9b2c749154c.png">

<img width="478" alt="image" src="https://user-images.githubusercontent.com/67833171/157563069-f983cd29-f57e-4528-9650-0e122b1e4546.png">
По сравнению с секвенированием ДНК или РНК можно заметить, что для графика per sequence quality scores к концу качество резко падает.
Что касается графика содержания GC, то у метилирования количество GC на чтение заметно отличается от теоритического показателя, что не cхоже с секвенированием ДНК или РНК. Кроме того, у метилирования наблюдаются два пика. 
График нуклеотидов в процентах у метилирования, в целом, более стабильный у начала, чем у секвенирования ДНК или РНК, но после одинаково выравниваются. Также здесь можно увидеть, что на графике нуклеотиды T и C имеют наибольшую схожесть в показателях, чем с остальными нуклеотидами, что отличается от секвенирования ДНК или РНК, где T/A и C/G более схожи в показателях.

## 2) Работа в colab:

### a. Число ридов, закартированных на участки

<img width="520" alt="image" src="https://user-images.githubusercontent.com/67833171/157553054-954457d1-69f2-49b8-99ce-6fe00528acb7.png">

### b. Дедупликация

<img width="620" alt="image" src="https://user-images.githubusercontent.com/67833171/157565146-f73647d3-5b11-404c-b6c6-9b258350d614.png">

### d. Отчет в формате html
По результатам отчета заметно, что больше метилирования в образце epiblast (77%), чем в других двух образцах. Далее идет 8cell (около 46%) и наименьшее значение имеет образец ICM (около 25%).

**Epiblast:**

<img width="907" alt="image" src="https://user-images.githubusercontent.com/67833171/157585493-398ede8f-ace2-458c-b257-0a8455a6f3a3.png">

**8cell:**

<img width="899" alt="image" src="https://user-images.githubusercontent.com/67833171/157583612-45db2ccc-907a-4e1a-96b1-688f104305d4.png">

**ICM:**

<img width="890" alt="image" src="https://user-images.githubusercontent.com/67833171/157586133-067dc56c-c85e-4a75-8411-ecb09ff31373.png">

### e. Гистограммы
**8cell:**

<img width="445" alt="image" src="https://user-images.githubusercontent.com/67833171/157581984-71fd276a-af05-48dd-873d-9d2c70ac5e03.png">

**Epiblast:**

<img width="452" alt="image" src="https://user-images.githubusercontent.com/67833171/157581818-0f0b4a5a-346d-4014-b661-fdb01cfeea0a.png">

**ICM:**

<img width="444" alt="image" src="https://user-images.githubusercontent.com/67833171/157582096-73b464d3-c6b9-4d5a-9708-63ee5b805c23.png">

Таким образом, это подтверждает различия в уровне метилирования на разных этапах развития эмбриона. То есть, наблюдаются волны деметилирования-метилирования: CpG метилирование 8cell (примерно 2.25 дня после оплодотворения яйцеклетки) уменьшается (до 45%), и так далее - на сроке примерно 3.5 дня после оплодотворения яйцеклетки (ICM) уровень метилирования становится еще ниже (25.5%). После, по мере дифференцировки тканей, происходит повышение CpG на сроке 6.5 дней и более (более 75%). То есть, уровень метилирования будет повышаться далее примерно до 90% и далее испытает еще волну
