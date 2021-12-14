# Final-SimpleDiary
SimpleDiary= Datepicker를 통해 날짜를 선택하였을때, 날짜에 일기가 없으면 새로 작성하고 있으면 일기를 보여주는 앱

[코드 주소] https://github.com/seoyoonjae/Final-SimpleDiary.git

### [Activity 코드 설명]

-  spinner 사용

-  일기가 저장되고 쓸 수 있는 자리 weight 써서 고정

-  버튼을 초기에 작동하지 못하게 하기 위해서 enabled 속성을 false 설정

### [MainActivity 코드 설명]

-  [Bundle saveInstaceState 객제]->앱을 중단할 때 임시적으로 데이터를 저장할 수 있게 설정

-  [fileName = Integer.toString(year) + "_" + Integer.toString(monthOfYear + 1) + "_" + Integer.toString(dayOfMonth) + ".txt";] ->한달은 0부터 시작이 되어서 10을 선택해도 9가 되기 때문에 1을 더하는 코드

-  String str = readDiary(fileName); ->현재의 날짜를 불러오는 메서드 작성

-   [try { inputStream = openFileInput(fName);
            byte[] txt = new byte[500];
            inputStream.read(txt);
            inputStream.close();
            diaryStr = (new String(txt)).trim();
            btnWrite.setText("수정하기");] ->작성한 일기가 있다면 수정하기 버튼을 눌러 수정할 수 있게 설정
            
            
-  [catch (IOException e) {
            editDiary.setHint("일기 없음");
            btnWrite.setText("새로 저장");] ->작성한 일기가 없으면 새로 작성하여 저장할 수 있게 설정
            


