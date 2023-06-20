FROM continuumio/miniconda3:latest
# Добавляем и делаем рабочей папкой /app
WORKDIR /app
# Скопируем 1.sh в контейнер с выдачей прав на исполнение
ADD --chmod=755 https://raw.githubusercontent.com/adtitovich/mlop-11/main/m1/1.sh /app
# Запускаем установку пакетов
RUN pip install --no-cache-dir --upgrade pip \
  && pip install --no-cache-dir mlflow boto3 pymysql
# запускаем на вывод файл 1.sh
CMD ["/1.sh"]
