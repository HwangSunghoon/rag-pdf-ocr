# RAG_PDF_OCR

## 📌 Overview (English)

This project implements a Retrieval-Augmented Generation (RAG) pipeline for PDF documents using OCR and LLMs.
It extracts text from PDFs, builds a retrieval system, and enables intelligent question answering.

The system is designed with a modular architecture and supports deployment via Docker and Kubernetes.

---

## 📌 개요 (Korean)

본 프로젝트는 PDF 문서를 OCR로 처리하고, Retrieval-Augmented Generation(RAG)을 활용하여
문서 기반 질의응답을 수행하는 시스템입니다.

문서 텍스트를 추출하고, 검색 기반 응답을 생성하며,
Docker 및 Kubernetes 환경에서 실행 가능하도록 설계되었습니다.

---

## 🚀 Features

* PDF OCR (문서 텍스트 추출)
* RAG 기반 검색 및 질의응답
* LLM 기반 응답 생성
* Backend / UI 분리 구조
* Docker Compose 실행 지원
* Kubernetes 배포 지원 (Deployment, Service, PVC 포함)

---

## 🛠 Tech Stack

* Python
* OCR
* LLM (GGUF 기반 모델)
* Docker / Docker Compose
* Kubernetes (Minikube)

---

## 📂 Project Structure

```
backend/        # RAG 서버 및 API
ui/             # 사용자 인터페이스
llm/            # LLM 관련 구성
k8s/            # Kubernetes 배포 파일
docker-compose.yml
```

---

## 🖥️ Demo

### 📌 Application UI

<img src="./assets/ui.png" width="700"/>

---

### 🐳 Docker Environment

<img src="./assets/docker.png" width="700"/>

---

### ☸️ Kubernetes Deployment

<img src="./assets/k8s.png" width="700"/>

---

## ⚙️ How to Run (English)

### 1. Docker

```
docker-compose up --build
```

---

### 2. Kubernetes

```
kubectl apply -f k8s/
```

Check pods:

```
kubectl get pods
```

---

## ⚙️ 실행 방법 (Korean)

### 1. Docker 실행

```
docker-compose up --build
```

---

### 2. Kubernetes 배포

```
kubectl apply -f k8s/
```

Pod 확인:

```
kubectl get pods
```

---

## 💾 Model Setup

Large model files are **NOT included** in this repository.

Please download the required model manually and place it in the `model/` directory.

Example:

```
model/
 ├── ggml-model-Q4_K_M.gguf
 ├── mmproj-model-f16.gguf
```

---

## ⚠️ Notes

* 대용량 모델 파일은 GitHub에 포함되어 있지 않습니다.
* Kubernetes에서는 Persistent Volume(PV/PVC)을 사용하여 모델을 관리합니다.
* 최소 2개의 Pod 간 통신을 지원하는 구조로 설계되었습니다.

---

## 📌 Future Work

* 성능 최적화 (GPU 지원)
* 멀티 문서 처리 개선
* UI 기능 확장
* 클라우드 배포 (AWS / GCP)

---

## 📄 License

MIT License

