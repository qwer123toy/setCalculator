![img](https://github.com/user-attachments/assets/56ae887a-f9db-4a58-84fa-e4ec9736b0bd)


<br>

<h1 align="center">
제품 세트 주문 및 가격 계산 관리 시스템
</h1>
<p align="center">제품별 케이스, 포장지, 쇼핑백 등 구성품을 조합하여 세트 가격을 자동 계산하는 ASP 기반 웹 애플리케이션</p>
<p align="center">사용자가 효율적으로 세트 주문을 관리하고 정확한 가격을 산출할 수 있는 업무 특화 시스템</p>

---

<br>
## 라이선스

해당 프로젝트는 회사 내부 프로젝트라 소스는 비공개이지만, 주요 내용과 구조는 README에서 확인하실 수 있습니다.

## 📌 Contents

<p align="left">목차</p>
<p align="left">
  <a href="#what-is">What is?</a>  <br>
  <a href="#key-features">Key Features</a> <br>
  <a href="#development-setup">Development Setup</a> <br>
  <a href="#repository-structure">Repository Structure</a> <br>
  <a href="#authors">Authors</a>
</p>

<br>

## What is

### 1. 개요 및 목적

 - 본 시스템은 제품 세트 주문 시 필요한 케이스, 포장지, 쇼핑백 등의 구성품을 조합하여 자동으로 가격을 계산하는 웹 기반 플랫폼
 - 기존 수동 계산 방식에서 벗어나 정확하고 빠른 견적 산출을 통해 업무 효율성을 극대화
 - 제품 유형별(타월, 우산, 콤보) 맞춤형 계산 로직으로 복잡한 세트 구성도 간편하게 처리
 - 저장된 주문 내역을 통해 반복 주문 및 이력 관리가 가능하여 고객 서비스 품질 향상에 기여

### 2. 적용 환경 및 기술

- Windows 서버 + IIS 기반으로 운용
- ASP (Classic ASP), MSSQL, JavaScript, HTML, CSS 사용
- jQuery UI와 Bootstrap을 활용한 직관적이고 반응형 사용자 인터페이스 제공
- Excel 파일 업로드 기능으로 대량 데이터 처리 지원

---

<br>

## Key Features

| 기능 영역 | 주요 기능 설명 |
|-----------|----------------|
| **세트 계산 기능** | - 제품 구분별(타월/우산/콤보) 맞춤형 계산<br> - 케이스, 포장지, 쇼핑백 조합별 자동 가격 산출<br> - 실시간 계산 결과 표시 및 수량별 단가 적용 <br> - 계산한 자료 Excel 파일 저장 |
| **주문 관리 기능** | - 세트 주문 등록 / 조회 / 수정 / 삭제<br> - 주문 내역 저장 및 이력 관리<br> - 검색 및 정렬 기능으로 효율적인 데이터 관리 |
| **관리자 기능** | - 제품 정보 및 가격 관리<br> - 분류별 제품 등록 및 수정 |
| **사용자 편의 기능** | - 직관적인 단계별 입력 폼<br> - 실시간 유효성 검사<br> - 반응형 디자인으로 다양한 디바이스 지원 |

---

<br>

## Development Setup

본 시스템은 ASP 및 MSSQL 기반의 기업용 세트 계산 전용 시스템으로, 다음과 같은 구성과 절차를 통해 개발

* **프로젝트 구조**
 - Classic ASP (VBScript) 기반 서버 사이드 스크립트로 구현
 - Microsoft IIS를 웹서버로 사용하여 내부망에서 서비스 제공
 - MSSQL Server를 RDBMS로 사용하여 제품 정보 및 주문 데이터 저장
 - JavaScript, jQuery, HTML, CSS를 통해 프론트엔드 UI 구성
 - Bootstrap 기반 반응형 디자인으로 일관된 UX 제공
 - 공통 DB 연결과 로직은 includes 폴더에서 통합 관리
 
 * **개발 절차 및 방법론**
 - 제품 세트 구성 및 가격 계산 로직 분석을 통한 요구사항 도출
 - 데이터베이스 설계 : 제품, 분류, 가격 정보를 효율적으로 관리하는 테이블 구조
 - 각 기능은 모듈별로 개발 후 AJAX를 활용한 동적 연동 구현
 - 제품 유형별 계산 로직 차별화로 정확한 가격 산출 보장
 - Excel 저장, 실시간 계산, 데이터 검증 등 실무 기능 통합 구현

 * **주요 개발 내용**
 - 세트 계산기 메인 페이지 및 계산 로직 구현
 - 제품별 분류 관리 및 동적 옵션 로딩 기능
 - 주문 내역 저장, 조회, 관리 시스템
 - 관리자 페이지를 통한 제품 정보 및 가격 관리
 - 사용자 친화적 UI/UX 디자인 및 반응형 웹 구현
 - 계산한 자료를 Excel 파일로 저장 가능

---

<br>

## Repository Structure

```bash
setCalculator/
├── setCalculator_250509.asp          # 메인 계산기 페이지
├── setCalculatorList_250325.asp      # 주문 내역 목록 페이지
├── setCalculatorAdmin.asp            # 관리자 페이지
├── setCalculatorAddProduct.asp       # 제품 추가 페이지
├── setCalculatorSaveProduct.asp      # 제품 저장 처리
├── setCalculatorLoadProduct.asp      # 제품 로드 처리
├── setCalculatorDeleteProduct.asp    # 제품 삭제 처리
├── setCalculatorDeleteUser.asp       # 사용자 삭제 처리
├── setCalculator_get_classifications.asp  # 분류 정보 API
├── setCalculator_get_case_options.asp     # 케이스 옵션 API
├── select_pcode_stockForSetCalc.asp       # 제품 재고 조회
├── SetExcelFileUpload.asp            # Excel 파일 업로드 처리
├── temp_line.txt                     # 임시 데이터 파일
├── .gitignore                        # Git 제외 파일 설정
└── README.md                         # 프로젝트 설명서
```

<br>

## 주요 기능 소개

### 🧮 세트 계산기
- **다단계 입력 폼** : 주문명 → 제품 구분 → 상세 옵션 → 계산 결과 순차 진행
- **실시간 계산** : 입력값 변경 시 즉시 가격 재계산 및 결과 표시
- **제품별 맞춤 계산** : 타월, 우산, 콤보 제품별 차별화된 계산 로직
- **Excel 업로드** : 세트 계산 정보를 Excel 파일로 저장

### 📋 주문 관리
- **주문 내역 저장** : 계산 완료된 세트 정보를 데이터베이스에 저장
- **검색 및 필터링** : 주문명, 제품명 등으로 빠른 검색 가능
- **페이지네이션** : 대량 데이터도 효율적으로 탐색

### ⚙️ 관리자 기능
- **제품 정보 관리** : 분류별 제품 등록, 수정, 삭제
- **가격 관리** : 제품별 단가 및 수량별 할인 정책 설정


<br>

## Authors
> 프로필 
>
> 이재민 [@깃허브 프로필 페이지](https://github.com/qwer123toy)
> 
