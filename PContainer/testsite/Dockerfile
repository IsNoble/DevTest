# Dockerfile

# Use official python runtime as the parent image
FROM python:3.9

# Allows docker to cache installed dependencies between builds
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Mount application code to the image
COPY . code
WORKDIR \CODE

EXPOSE 8000

# Run the production server
ENTRYPOINT [ "python", "testsite\manage.py" ]
CMD [ "runserver", "0.0.0.0:8000" ]