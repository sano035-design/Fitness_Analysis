# 📊 Fitness Activity Standardization & Analysis (Bill, Ben, Bob)

This project demonstrates the process of standardizing and merging three disparate fitness datasets into a single, unified Power BI dashboard.

## 📁 Repository Structure

* **data/**: Contains raw exercise logs for Bill, Ben, and Bob.
* **powerbi/**: Includes the final `Fitness_Analysis.pbix` file.
* **README.md**: Documentation of the data transformation and insights.

## 🛠️ Data Transformation (Power Query)

To ensure data consistency before merging (Appending), the following **M-Code** transformations were applied:

1. **Text Extraction**: Used `Text.BetweenDelimiters` to extract specific activity names (e.g., "cycling") from sentence-based logs[cite: 1, 4].
2. **Normalization**: Converted all activity names to **lowercase** to prevent duplication during merging[cite: 1, 4].
3. **Unpivoting (Wide to Long)**: Transformed columns into multiple rows, splitting them into 'Attribute' (Week) and 'Value' (Hours)[cite: 5, 6].
    > *Logic:* `Table.UnpivotOtherColumns(Source, {"Column1"}, "Attribute", "Value")`
4. **Pivoting (Long to Wide)**: For the final analysis format, 'Weeks' were set as columns and 'Activities' as rows[cite: 7, 8, 12].
5. **Identification**: Added a **Custom Column** named `name` for each table (e.g., "Bill", "Ben", "Bob") before merging to identify the data source[cite: 9, 10].
6. **Appending**: Merged the three standardized tables into a single query named `Append3`[cite: 13, 14].



## 🔍 Key Insights & Dashboard Preview

### **Key Insights**
* **Unified Visibility**: Successfully merged three different data formats into one master table[cite: 13, 14].
* **Top Performer**: Based on the 4-week aggregate data, **Bill** recorded the highest total exercise hours (18.0 hours)[cite: 15].
* **Activity Trends**: Identified individual preferences across Swimming, Running, and Cycling through visual comparison[cite: 15].

### **Dashboard Preview**
![Fitness Dashboard Preview](https://example.com/your-dashboard-screenshot.png)
[cite_start]*Figure 1: Stacked Bar Chart showing Total Hours by Name and Activity [cite: 15]*

![Data Summary Table](https://example.com/your-table-screenshot.png)
[cite_start]*Figure 2: Summary Table displaying Name, Activity, and Weekly Hours (Week 1-4) [cite: 15]*

## 🚀 How to Use

1. **Load Project**: Open `powerbi/Fitness_Analysis.pbix`.
2. **Refresh Data**: Click `Close & Apply` to load the transformed data into the report view.
3. **Interact**: Use the **Activity Slicer** or **Name Filter** to explore specific trends.


# 📊 Personal Fitness Activity Analysis (Bill, Ben, Bob)

[cite_start]이 프로젝트는 Bill, Ben, Bob 세 명의 서로 다른 데이터 포맷을 Power BI를 통해 표준화하고 병합하여, 4주간의 운동 성과를 분석한 프로젝트입니다. [cite: 1, 2]

## 📁 Repository Structure

* [cite_start]**data/**: Bill, Ben, Bob의 개별 운동 데이터 (Excel/CSV) [cite: 3, 11]
* **powerbi/**: 최종 분석 결과가 포함된 `Fitness_Analysis.pbix` 파일
* **screenshots/**: 데이터 변환 과정 및 대시보드 캡처 이미지

## 🔍 Key Insights

* [cite_start]**데이터 통합 성공**: 각기 다른 형태(Wide & Long Format)의 데이터를 하나의 마스터 테이블로 통합했습니다. [cite: 1, 13]
* [cite_start]**최고 활동량 기록**: 4주간의 전체 운동 시간을 합산한 결과, **Bill**이 가장 높은 활동량을 기록했습니다. [cite: 15]
* [cite_start]**종목별 선호도**: 수영(Swimming), 달리기(Running), 사이클링(Cycling) 중 개인별로 집중한 종목의 차이를 시각적으로 확인했습니다. [cite: 15]

## 🛠️ Data Transformation (Power Query)

[cite_start]데이터의 일관성을 확보하기 위해 다음과 같은 **표준화 과정**을 수행했습니다: [cite: 2]

1. **데이터 추출 (Extraction)**: 텍스트 문장에서 "cycling"과 같은 운동 종목만 추출했습니다.
2. **소문자 변환 (Normalization)**: 데이터 비교의 정확성을 위해 모든 종목명을 소문자(lowercase)로 통일했습니다.
3. [cite_start]**피벗 해제 (Unpivoting)**: 열로 나열된 데이터를 행으로 변환하여 분석에 적합한 구조로 재구성했습니다. [cite: 5, 6]
    * [cite_start]이 과정에서 컬럼 값이 여러 행으로 바뀌며 'Attribute'와 'Value'로 나눠집니다. [cite: 6]
4. [cite_start]**열 피벗 (Pivoting)**: 분석 목적에 따라 'Week'를 열(Column)로, 'Activity'를 행(Row)으로 배치했습니다. [cite: 4, 7, 8, 12]
5. [cite_start]**식별자 추가 (Identification)**: 병합 전, 각 데이터의 소유자를 구분하기 위해 `name` 컬럼을 생성하고 "Bill", "Ben", "Bob" 등의 값을 부여했습니다. [cite: 9, 10]
6. [cite_start]**쿼리 병합 (Appending)**: 표준화된 세 개의 테이블을 `Append` 기능을 사용하여 하나로 합쳤습니다. [cite: 13, 14]



## 🚀 How to Use

1. **Power BI 실행**: `powerbi/Fitness_Analysis.pbix` 파일을 엽니다.
2. **데이터 로드**: `Close & Apply`를 눌러 변환된 데이터를 시각화 화면으로 가져옵니다.
3. **분석**: 이름(name)과 종목(Activity) 필터를 사용하여 개인별 운동 추이를 확인합니다.

## 📊 Dashboard Preview

* [cite_start]**Table Visual**: 이름별 종목 및 주차별 운동 시간 합계 표시 [cite: 15]
* [cite_start]**Total Hours Chart**: 4주 누적 합산 시간을 보여주는 스택형 막대 차트 [cite: 15]
