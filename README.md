# 📊 Data Structure Benchmark

## 📌 Overview

* Dataset Size: **200,000 elements**
* Search Sample: **1,000**
* Benchmark Source: raw benchmark log

---

## ⚡ Performance Summary

| Data Structure | Insert (ms) | Search (ms) | Sort (ms) | Memory (MB) |
| -------------- | ----------- | ----------- | --------- | ----------- |
| **HashTable**  | ~50–60      | ~0          | 0         | ~70         |
| **BTree**      | ~260–320    | ~2–3        | 0         | ~80         |
| **LinkedList** | ~9–24       | ~7000+      | ~500k+    | ~87         |
| **ArrayList**  | ~26–27      | ~3700–4600  | ~185–205  | ~95         |
| **Vector**     | ~28–36      | ~3600–4500  | ~190–449  | ~103        |
| **Graph**      | ~130–165    | ~1          | 0         | ~150        |
| **Heap**       | ~57–89      | ~3200–4400  | 0         | ~140–159    |

---

## 🔍 Detailed Insights

### 🥇 Fastest Overall: HashTable

* 압도적인 검색 성능 (≈ 0ms)
* 삽입도 매우 빠름
* 메모리 효율도 준수

👉 대부분의 lookup-heavy 작업에 최적

---

### 🥈 Balanced Structure: B-Tree

* 삽입은 느리지만 안정적
* 검색 성능도 빠른 편

👉 DB / 인덱싱 구조에 적합

---

### ⚠️ LinkedList

* 삽입은 매우 빠름
* 검색: 매우 느림 (~7000ms)
* 정렬: 매우 비효율 (~500,000ms)

👉 순차 접근 외에는 비추천

---

### 📦 ArrayList vs Vector

* 성능 거의 유사
* Vector는 약간 더 느리고 메모리 더 사용

👉

* ArrayList → 일반 사용
* Vector → thread-safe 필요 시

---

### 🌐 Graph

* 검색 성능 매우 우수 (~1ms)
* 메모리 사용량 큼

👉 관계형 데이터에 적합

---

### 🔺 Heap

* 삽입은 빠름
* 검색은 느림

👉 우선순위 큐에 적합

---

## 📈 Key Takeaways

* 🔥 검색 속도 중요 → HashTable
* ⚖️ 균형 → BTree
* 🚫 LinkedList는 검색/정렬 비효율
* 📦 일반 리스트 → ArrayList
* 🧠 특수 구조는 목적에 맞게 사용

---

## 🧪 Notes

* 여러 번 실행해도 결과는 일관됨
* 각 자료구조는 목적에 따라 성능 차이 존재
