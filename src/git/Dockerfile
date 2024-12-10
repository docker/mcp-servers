FROM python:3.10-alpine

RUN apk add --no-cache git

WORKDIR /project

COPY . .

RUN pip install .

CMD ["python", "-m", "mcp_server_git"]
