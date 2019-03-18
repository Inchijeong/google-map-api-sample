Google Place API 사용하기
========================

들어가기 전에
------------

1. 사용 요금 정책을 먼저 확인하도록 한다.
2. 구글 콘솔에 사용할 프로젝트를 만들어야한다.
3. API 를 사용하기 위해서는 2에서 만든 프로젝트의 해당 API의 Key를 발급받아야 한다.(API키 활성화)
4. 서버쪽에서 사용하는 API 와 클라이언트(Javascript) 에서 사용하는 방식이 다르다. 즉, 다른 Docs 를 찾아봐야한다.

순서
---

1. 구글 로그인
2. 'place api javascript' 또는 'maps javascript api' 검색
3. [Map Javascript API](https://developers.google.com/maps/documentation/javascript/places) 해당 사이트 접속
4. 좌측 네이비게이션에서 Get API Key 클릭  
    ![4번 설명 이미지](./img/3.png)
5. 해당 내용을 읽어보고 'Google Cloud Platform Console로' 클릭.

6. 1번 부분 누르고 2-1 눌러서 신규 프로젝트 생성 또는 2-2로 프로젝트 선택 후 OPEN  
    ![6-1번 설명 이미지](./img/4.png)

    6-2. 신규 프로젝트 생성할 경우 간단히 이름 설정과 디렉토리 경로를 설정해서 생성 가능하다.  
    ![6-2번 설명 이미지](./img/5.png)  

7. 좌측 메뉴에서 Dashboard 탭에  '+ENABLE APIS AND SERVICES' 클릭하면 프로젝트에서 사용할 API 를 추가할 수 있다.  
    ![7번 설명 이미지](./img/6.png)  

8. 'Maps JavaScript API' , 'Place API' 등 사용할 API 클릭  
    ![8번 설명 이미지](./img/7.png)  

9. 'ENABLE' 클릭하면 APIs 탭에 추가된 것을 확인할 수있다.  
    ![9번 설명 이미지](./img/8.png)  

발급 받고자 하는 API 를 클릭한다.  
    ![9-2번 설명 이미지](./img/9.png)  

10. 'Create credentials' 클릭하면 팝업이 뜨는데 'API key' 클릭하자 그러면 해당 API를 사용할 수 있는 키를 발급해준다.  
    ![10번 설명 이미지](./img/10.png)  
    ![10-2번 설명 이미지](./img/11.png)  

11. 다시 3번의 [Map Javascript API](https://developers.google.com/maps/documentation/javascript/places) 사이트로 돌아와 참조.

프로젝트에서 아래 코드를 삽입시킨다.

<script type="text/javascript" src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&libraries=places"></script>

발급받은 키를 YOUR_API_KEY 에 넣어준다.

12 . 이제 사용할 js파일에 아래의 코드를 수정해서 사용하면 된다.  
    ![12번 설명 이미지](img/12.png)  



위 6라인의 PlacesService(map) 에 인자값으로 map 객체가 아닌 기본 노드가 들어갈 수있음.

service = new google.maps.places.PlacesService(document.createElement('div'));
처럼 변경 가능

참조 : <https://stackoverflow.com/questions/14343965/google-places-library-without-map>



13. [Inchijeong place_API 예제](https://github.com/Inchijeong/google_place_API) 사이트에 가서 place.html
  key 부분을 수정해 주고 입맛에 맞춰 js를 수정해 사용한다.














