# Usa una imagen base de Python
FROM python:3.11

# Instala pip y las dependencias necesarias
RUN pip install --upgrade pip
RUN pip install pandas matplotlib scikit-learn

# Establece el directorio de trabajo
WORKDIR /app

# Copia el archivo de script al contenedor
COPY iris_visualizer.py .

# Comando por defecto para ejecutar el script
CMD ["python", "iris_visualizer.py"]
