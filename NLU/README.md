# 한국어 자연어 이해 (KLUE Benchmark)  
(Pure PyTorch Loop & 🤗 Trainer)

이 레포는 **KLUE(Korean Language Understanding Evaluation)** 벤치마크의 **8개 NLU Task**를 대상으로  
- **Pure PyTorch 커스텀 학습 루프**  
- **🤗 Transformers Trainer 기반 구현**  

두 가지 방식을 모두 제공하는 프로젝트입니다. 모두 google Colab에서 동작 가능합니다!

---

## 📌 KLUE 8개 Task

1. **YNAT (Topic Classification)**  
   - 뉴스 기사 제목을 7개 주제(IT과학, 경제, 사회, 생활문화, 세계, 스포츠, 정치)로 분류

2. **NLI (Natural Language Inference)**  
   - 두 문장 간 관계 (Entailment / Contradiction / Neutral)

3. **STS (Semantic Textual Similarity)**  
   - 두 문장 의미 유사도를 0~5 범위 점수로 예측

4. **NER (Named Entity Recognition)**  
   - 문장에서 개체명(사람, 장소, 기관, 날짜 등) 추출

5. **RE (Relation Extraction)**  
   - 두 개체 간 관계 판별 (예: "A는 B의 아버지" → Parent-of)

6. **DP (Dependency Parsing)**  
   - 문장의 구문 구조를 의존 구문 트리로 분석

7. **MRC (Machine Reading Comprehension)**  
   - 지문을 읽고 질문에 대한 정답 span 추출

8. **Dialogue (Dialogue State Tracking, DST)**  
   - 멀티턴 대화에서 사용자 의도와 슬롯 값을 추적

---

## ⚙️ 구현 방식

- **PyTorch 학습 루프**
  - Dataset/DataLoader 구성  
  - Optimizer, Scheduler, Loss, Metrics 직접 구현  
  - Accuracy, F1, classification_report, confusion matrix 지원

- **Trainer 기반**
  - `TrainingArguments`, `Trainer`, `compute_metrics` 활용  
  - 자동 로깅, 체크포인트, 평가  
  - TensorBoard/W&B 연동 가능

---

## 🚀 목표

- KLUE 전체 8개 태스크에 대해 **엔드투엔드 학습 파이프라인** 제공  
- **PyTorch vs Trainer** 비교를 통한 구현 방식 이해  
- 한국어 NLU 태스크 벤치마크 실험을 **재현 가능**하게 제공  

---

📜 참고

- KLUE Benchmark: https://klue-benchmark.com

- Hugging Face Datasets: https://huggingface.co/datasets/klue

