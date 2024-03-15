# model

1. model에 엑셀파일 추가/수정
    - null은 허용하지 않음(json 변경 시 오류 발생)
    - 확장자는 .xlsx로 고정
    - column:1(id)는 반드시 존재해야하는 컬럼
    - row 3줄은 필수로 있어야 함
        - row:1 - 컬럼명(중복되면 안됨)
        - row:2 - 기획자/프로그래머가 확인하기 위한 주석
        - row:3 - 타입(int/string/bool만 가능)

2. 로컬 서버 실행(/backend/01.START_LOCAL_SERVER.bat)

3. cmd창을 켜서 curl -X POST localhost:12237/parse?path={path} 입력
    - {path}는 해당 드라이브에서 절대 경로 ex) C:/GitHub/model -> /GitHub/model