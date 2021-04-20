# video_viewer_JS

JavaScript

error_1) (크롬에서) 로컬에서 CORS policy 관련 에러가 발생하는 경우!

-> Access to script at 'file:///C:/경로/*.json' from origin 'null' has been blocked by CORS policy: Cross origin requests are only supported for protocol schemes: http, data, chrome, chrome-extension, https.
-> Requests Headers에서 origin 값이 null로 보내짐.

conclusion_1-1) API 서버에서 "Access-Control-Allow-Origin : *"을 추가해주지 않으면, 크롬에서 "file://" URL로 API 데이터를 받아올 수 없음.
conclusion_1-2) 서버에서 API 데이터를 받아서 포워딩을 한 이후에 다시 데이터를 받아와야함.

solve_1) 아파치 서버에서 PHP 코드로 데이터 포워딩을 할 수 있음.

In code) mbcsports.mp4 영상은 2021.04.08 KIA vs. 키움 (고척) 경기를 사용하였음.
