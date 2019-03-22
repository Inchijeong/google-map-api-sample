# Google Place API 사용하기


## 들어가기 전에

1. 사용 요금 정책을 먼저 확인하도록 합니다.

2. 구글 콘솔에 사용할 프로젝트를 만들어야 합니다.

3. API 를 사용하기 위해서는 [2] 에서 만든 프로젝트의 해당 API의 Key를 발급받아야 합니다.(API키 활성화)

4. 서버쪽에서 사용하는 API 와 클라이언트(Javascript) 에서 사용하는 방식이 다릅니다.

   즉, 다른 Documentation 을 찾아봐야 합니다.



> Place Searches 라이브러리를 예시로 사용하였습니다.



## Google API 키 발급

1. 구글 로그인

2. 'place api javascript' 또는 'maps javascript api' 검색

3. <https://developers.google.com/maps/documentation/javascript/places> 해당 사이트 접속

4. 좌측 네이비게이션에서 Get API Key 클릭

5. 해당 내용을 읽어보고 'Google Clout Platform Console로' 클릭

   ![2041](https://user-images.githubusercontent.com/31085727/54803415-c4229080-4cb2-11e9-8557-30d1fb1526c6.png)

6. 

   6-1. 1번 부분 누르고, 2-1 눌러서 신규 프로젝트 생성 또는 2-2로 프로젝트 선택 후 OPEN

   ![2042](https://user-images.githubusercontent.com/31085727/54803416-c4229080-4cb2-11e9-994a-99f771eb99c7.png)

   6-2. 신규 프로젝트 생성할 경우 간단히 이름 설정과 디렉토리 경로를 설정해서 생성 가능합니다.

   ![2043](https://user-images.githubusercontent.com/31085727/54803417-c4229080-4cb2-11e9-9e1e-ac2b853c9604.png)

7. 좌측 메뉴에서 Dashboard 탭에  '+ENABLE APIS AND SERVICES' 클릭하면 프로젝트에서 사용할 API 를 추가할 수 있습니다.

   ![2044](https://user-images.githubusercontent.com/31085727/54803418-c4bb2700-4cb2-11e9-89d1-a33c30749978.png)

8. 'Maps JavaScript API' , 'Place API' 등 사용할 API 클릭

   ![2045](https://user-images.githubusercontent.com/31085727/54803419-c4bb2700-4cb2-11e9-8014-e6da6eeb5dbe.png)

9. 'ENABLE' 클릭하면 APIs 탭에 추가된 것을 확인할 수 있습니다.

   ![2046](https://user-images.githubusercontent.com/31085727/54803420-c4bb2700-4cb2-11e9-9a11-914c7635deb5.png)

10. 발급 받고자 하는 API 를 클릭

    ![2048](https://user-images.githubusercontent.com/31085727/54803423-c553bd80-4cb2-11e9-802a-8b2876559eed.png)

11. 'Create credentials' 클릭하면 팝업이 뜨는데 'API key' 클릭.

     그러면 해당 API를 사용할 수 있는 키를 발급해줍니다.

    ![2047](https://user-images.githubusercontent.com/31085727/54803422-c4bb2700-4cb2-11e9-91e5-1de634a54879.png)

    ![2049](https://user-images.githubusercontent.com/31085727/54803424-c553bd80-4cb2-11e9-94a6-9aa743632891.png)



## HTML에 Google API 추가



> <https://developers.google.com/maps/documentation/javascript/places> 의 Getting started 부분 참조.



1. 프로젝트에서 아래 코드를 삽입시킵니다.

   ```html
   <script type="text/javascript" src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&libraries=places"></script>
   ```

2. 발급받은 키를 YOUR_API_KEY 자리에 넣어줍니다.

3. 이제 doccumentation 을 살펴보면서 코드를 작성하세요.

![2050](https://user-images.githubusercontent.com/31085727/54803425-c553bd80-4cb2-11e9-9020-b5842b61212a.png)

*위 예제 코드 보충 설명*

위 6라인의 PlacesService(map) 에 인자값으로 map 객체가 아닌 기본 노드가 들어갈 수 있습니다.

`service = new google.maps.places.PlacesService(document.createElement('div'));`

처럼 변경 가능합니다.

참조 : <https://stackoverflow.com/questions/14343965/google-places-library-without-map>



------





저의 [Github](https://github.com/Inchijeong/google-map-api-sample)  placeAPI, map 등 여러 템플릿 코드를 업로드 중이니 클론해가셔도 좋습니다.

> YOUR_API_KEY 부분을 본인의 키를 삽입한 뒤 js를 상황에 맞게 수정하여 사용하세요.

