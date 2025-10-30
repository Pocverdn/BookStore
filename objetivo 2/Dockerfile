# Usa una imagen oficial de Python
FROM python:3.10-slim

# Establece el directorio de trabajo
WORKDIR /app

COPY requirements.txt requirements.txt

# Instala las dependencias
RUN pip install --no-cache-dir -r requirements.txt

# Copia los archivos al contenedor
COPY . .

# Expone el puerto 5000 para Flask
EXPOSE 5000

# Comando para correr la app
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "app.py"]
