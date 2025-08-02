# ARM/x86 모두 지원하는 공식 Python 이미지 사용
FROM python:3.10-slim

# 디폴트 설정
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# 컴파일용 빌드 툴 설치 (numpy 등 대비)
RUN apt-get update && apt-get install -y build-essential

# 작업 디렉토리 (컨테이너 내부)
WORKDIR /app

# requirements 복사 후 패키지 설치
COPY requirements.txt .
RUN pip install --upgrade pip && pip install -r requirements.txt
