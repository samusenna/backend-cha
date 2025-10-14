# Use Python 3.13 slim como base
FROM python:3.13-slim

# Variáveis de ambiente para evitar problemas de cache de pip
ENV PYTHONUNBUFFERED=1
ENV PIP_NO_CACHE_DIR=1

# Defina o diretório de trabalho
WORKDIR /app

# Copie o requirements.txt e instale as dependências
COPY requirements.txt .
RUN pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt

# Copie todo o código para dentro do container
COPY . .

# Exponha a porta que seu Flask vai rodar
EXPOSE 5000

# Comando para rodar a aplicação
CMD ["python", "api/main.py"]
