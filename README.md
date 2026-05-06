# OpenTrack

This project is a simple Python program for managing an open source project. 
It stores project information, contributors, and issues using Python data structures such as tuples, lists, dictionaries, and sets.  
It also analyzes issue data and saves the results into text and CSV files.

## Environment
- **Platform**: Google Colab (Recommended) or Local Python Environment
- **Language**: Python 3.x

## Libraries Used (Imports)
This project uses built-in Python standard libraries, so no additional installation via `pip` is required:
- `os`: Used for creating project folders and managing file paths.

## Main Functions
- Store project information (Immutable data handled via Tuples)
- Manage contributors list (List of Dictionaries)
- Track and analyze issues (Priority and Status grouping)
- Set operations for tech stack and reporter analysis
- File handling: Save and read project reports and CSV data

## How to Run
### Option 1: Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new notebook.
3. Copy the code from `main.py` and paste it into a code cell.
4. Run the cell (Shift + Enter).
5. Input the requested information (Contributor/Issue details) in the interactive prompts.
6. After execution, check the sidebar folder icon to find the generated `opentrack/` directory.

### Option 2: Local Environment
1. Ensure you have Python installed.
2. Save the code as `main.py`.
3. Run the following command in your terminal:
   ```bash
   python main.py

### Output Files
The program automatically creates an opentrack/ folder and generates:

project_report.txt: A full summary of the project, including urgent issues.

issues.csv: A structured list of tracked issues.

프로젝트 개요 (Korean)
이 프로젝트는 오픈소스 프로젝트 관리를 위한 간단한 파이썬 프로그램입니다. 튜플, 리스트, 딕셔너리, 집합 등 파이썬의 핵심 자료구조를 활용하여 프로젝트 정보, 기여자, 이슈 데이터를 관리하며, 분석 결과는 텍스트(txt) 및 CSV 파일로 저장됩니다.

실행 환경
플랫폼: Google Colab (권장) 또는 로컬 파이썬 환경

언어: Python 3.x

사용 라이브러리 (Import)
별도의 외부 설치 없이 파이썬 표준 라이브러리를 사용합니다.

os: 폴더 생성 및 파일 경로 관리를 위해 사용되었습니다.

실행 방법
옵션 1: Google Colab 사용 시 (권장)
Google Colab에 접속합니다.

새 노트북을 생성합니다.

main.py의 코드를 복사하여 셀에 붙여넣습니다.

셀을 실행(Shift + Enter)합니다.

화면에 나오는 안내에 따라 기여자 정보와 이슈 정보를 입력합니다.

실행이 완료되면 왼쪽 사이드바의 '폴더' 아이콘을 클릭하여 생성된 opentrack/ 폴더 내 결과 파일을 확인합니다.

옵션 2: 로컬 환경 사용 시
코드를 main.py 파일로 저장합니다.

터미널(또는 CMD)에서 아래 명령어를 실행합니다.

Bash
python main.py
생성 결과물
프로그램 실행 시 opentrack/ 폴더 내에 다음 파일이 자동 생성됩니다.

project_report.txt: 긴급 이슈를 포함한 전체 프로젝트 요약 보고서

issues.csv: 구조화된 이슈 목록 데이터
