FROM SVDCPFCP01.mozabanco.co.mz/moza-hub-release/python:3.14-slim-trixie


WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir \
    --index-url http://10.111.2.43:8081/nexus/repository/pypi-group/simple/ \
    --trusted-host 10.111.2.43 \
    -r requirements.txt

COPY . .

CMD ["python", "-m", "uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]