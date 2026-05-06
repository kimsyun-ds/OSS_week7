### OpenTrack Documentation
## 1. Project Overview
OpenTrack is a Python-based management system designed to collect, process, and analyze data for open-source projects. It handles contributor details and issue tracking through various Python data structures.

## 2. Key Variables & Data Structures
The program strategically uses different data structures to manage project data efficiently:

project (Tuple): Stores constant information such as the project name, version, and start year. Since these values should not be modified, a Tuple is used for its immutability.

contributors (List of Dictionaries): A dynamic list that stores multiple dictionary objects, each representing a contributor's profile.

issues (List of Dictionaries): A list used to track issue details including IDs, titles, and priorities.

reporters & tech_stack (Set): Utilized to extract unique values and perform set operations. Sets ensure that there are no duplicate names or languages in the analysis.

priority_count (Dictionary): Maps issue priority levels (Keys) to their frequency (Values) for statistical reporting.

status_groups (Dictionary): Groups issue titles based on their current status (e.g., Open, In Progress, Resolved).

## 3. Core Functions & Methods
The following built-in functions and methods are used for data manipulation and file management:

Data Processing
input(): Captures real-time data from the user regarding contributors and issues.

print(): Displays the project banner, analysis results, and process logs on the console.

list.append(): Adds new data entries to the end of the contributors and issues lists.

list.sort(): Organizes the contributor names in alphabetical order.

dict.update() / dict.pop(): Used to modify records by adding new status keys or removing unnecessary metadata (e.g., removing the 'type' key).

set.union(), intersection(), difference(): Performs logical comparisons between the list of reporters and the project's technical stack.

String & File Handling
str.lower() / str.replace(): Formats the project name into a standardized folder name (e.g., "OpenTrack" becomes "opentrack").

os.mkdir() / os.path.exists(): Checks for the existence of a directory and creates it if it does not exist to ensure safe file saving.

open() (with w, r, a modes):

'w' (Write): Creates new report and CSV files.

'r' (Read): Retrieves data from existing files to display in the console.

'a' (Append): Adds an "Urgent Issues" section to the end of an existing report without overwriting it.

file.read(), readline(), readlines(): Demonstrates different methods of data retrieval from text files, from reading the entire content to processing it line-by-line.

## 4. Logical Flow
Initialization: Sets up core project data and displays the interface header.

Data Acquisition: Uses for loops to gather information for 4 contributors and 5 issues.

Data Analysis: Identifies the "Top Reporter," counts open issues, and filters "Critical" tasks.

File Export: Utilizes the os module and try-except blocks to securely save the analysis into a dedicated project folder.

## 5. Output Files
project_report.txt: A comprehensive text-based summary of all project data.

issues.csv: A structured data file compatible with spreadsheet software like Excel.

OpenTrack Documentation
1. Project Overview
OpenTrack은 사용자로부터 데이터를 입력받아 오픈소스 프로젝트의 구성원과 이슈를 관리하고 분석하는 Python 기반 프로그램입니다.

2. Key Variables & Data Structures (변수 및 자료구조)
프로그램의 목적에 따라 다양한 파이썬 자료구조를 변수로 활용하였습니다.

project (Tuple): 프로젝트 이름, 버전, 시작 연도 등 변경되어서는 안 되는 고정 데이터를 저장합니다. (Immutable 특성 활용)

contributors (List of Dictionaries): 기여자 정보를 담은 여러 개의 딕셔너리를 리스트 형식으로 관리합니다.

issues (List of Dictionaries): 발생한 이슈들의 상세 정보(ID, 제목, 우선순위 등)를 저장하는 리스트입니다.

reporters & tech_stack (Set): 이슈 보고자와 사용된 기술 스택의 중복을 제거하고 고유한 값만 추출하거나 집합 연산을 수행하기 위해 사용합니다.

priority_count (Dictionary): 이슈의 우선순위(Critical, High 등)를 키(Key)로, 해당 빈도수를 값(Value)으로 하여 데이터를 집계합니다.

status_groups (Dictionary): 이슈 상태(Open, In Progress 등)에 따라 이슈 제목들을 그룹화하여 저장합니다.

3. Core Functions & Methods (주요 함수 및 메서드)
코드 내에서 데이터 처리와 파일 관리를 위해 사용된 주요 기능들입니다.

Data Processing (데이터 처리)
input(): 사용자로부터 기여자 및 이슈 정보를 직접 입력받습니다.

print(): 분석 결과와 프로젝트 배너, 처리 과정을 화면에 출력합니다.

list.append(): 입력받은 새로운 데이터를 리스트에 순차적으로 추가합니다.

list.sort(): 기여자 이름을 알파벳 순서로 정렬합니다.

dict.update() / dict.pop(): 딕셔너리에 새로운 항목(상태 정보)을 추가하거나 특정 항목(타입 정보)을 제거합니다.

set.union(), intersection(), difference(): 집합 연산을 통해 보고자와 기술 스택 간의 관계를 분석합니다.

String & File Handling (문자열 및 파일 처리)
str.lower() / str.replace(): 프로젝트 이름을 소문자로 변경하고 공백을 언더스코어(_)로 바꿔 폴더명을 생성합니다.

os.mkdir() / os.path.exists(): 폴더가 존재하는지 확인하고, 없을 경우 새로운 작업 디렉토리를 생성합니다.

open() (with w, r, a modes):

'w': 보고서 및 CSV 파일을 새롭게 작성합니다.

'r': 저장된 파일을 읽어와 내용을 확인합니다.

'a': 기존 보고서 파일 끝에 긴급 이슈 목록을 추가(Append)합니다.

file.read(), readline(), readlines(): 파일의 전체 내용, 한 줄, 또는 모든 줄을 리스트 형태로 읽어오는 다양한 방식을 구현했습니다.

4. Logical Flow (로직 흐름)
Setup: 프로젝트 기본 정보를 설정하고 배너를 출력합니다.

Collection: 반복문(for)을 통해 사용자로부터 기여자 4명과 이슈 5개의 정보를 입력받습니다.

Analysis: 조건문과 반복문을 사용하여 'Open' 상태의 이슈 개수, 최다 보고자, 긴급 이슈 등을 분석합니다.

Storage: os 모듈과 예외 처리(try-except)를 활용하여 분석 데이터를 파일로 안전하게 저장하고 다시 읽어옵니다.

5. Output Files
project_report.txt: 분석 결과 요약 및 상세 로그

issues.csv: 엑셀 등에서 확인 가능한 이슈 데이터 시트
