create folder myproj and cd myproj 
create the simpliest fastapi file:
```
from fastapi import FastAPI
from fastapi.responses import HTMLResponse
 
app = FastAPI()

@app.get("/")
def read_root():
    html_content = "<h2>Hello world!</h2>"
    return HTMLResponse(content=html_content)

```
create dockerfile:
```
FROM ubuntu
COPY . /root/hello-world
WORKDIR /root/hello-world
EXPOSE 80

RUN apt update
RUN apt install -y python3
RUN apt install -y python3-pip
RUN apt install -y python3-venv

RUN python3 -m venv venv

```
build dockerfile and run container:
```
docker build -t my-image .
docker run -p 80:80 -it my-image
```
in ubuntu console we need to activate venv and install libs:
```
source ./venv/bin/activate
pip install fastapi uvicorn
```
and run uvicorn with proper host and port:
```
uvicorn main:app --host 0.0.0.0 --port 80
```
Profit!