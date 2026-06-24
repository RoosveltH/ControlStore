# Imagen base de Python
FROM python:3.11-slim

# Directorio de trabajo
WORKDIR /app

# Copiar dependencias
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copiar el c�digo del backend
COPY . .

# Exponer el puerto
EXPOSE 8000

# Comando por defecto (Gunicorn para producci�n)
CMD ["gunicorn", "proyecto.proyecto.wsgi:application", "--bind", "0.0.0.0:8000"]


