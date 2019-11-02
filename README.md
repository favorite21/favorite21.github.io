LSB homepage management notice

1. Home
- 대부분 _ config.yml에서 변경할 수 있음
![ex_screenshot](/assets/img/homepage_management.png)

- column 설정
~~~
<div class="col-숫자">
~
</div>
~~~
까지 하나의 column

현재 Home.html에는 column이 두 개 있음(좌, 우).

"col-숫자" 에서 숫자에 들어갈 수 있는 수는 1~12까지 가능(default는 6임-왠만하면 바꿀일 없음.)

- Slide 사진 변경

슬라이드에는 사진이 총 4개까지 출력되도록 설정해 두었음.

~~~
		        <div class="slide"><img src="/assets/img/home1.png">Electron density map</div>
                        <div class="slide"><img src="/assets/img/home2.png">Chitinase</div>
                        <div class="slide"><img src="/assets/img/home3.png">HslV-HslU complex</div>
                        <div class="slide"><img src="/assets/img/home4.jpg">Protein Crystals</div>
~~~

에서 각 표시될 사진들을 assets/img에 저장하고 주소를 불러올 것. 이후 해당 사진에 관한 간단한 설명.

- 폰트 사이즈 밑 굵기 설정

  `<p style="font-size:0.9rem;font-weight:300">`

에서 ref과 weight 수정

2. About, Members, Experimetal, Publication, Useful link
- 각 폴더의 folder의 index.md에서 변경할 수 있음
- [md(markdown) concept 관련 참조](http://sergeswin.com/1013)

3. Gallery
- layouts/gallery.html에서 수정 가능

- 사진 추가 방법

~~~
   		<!-- picture -->
                <div class="container">
                    <a href="/assets/gallery/MTA.pdf"><img src="/assets/gallery/MTA.jpg" alt="Avatar" class="image"><a>
                    <div class="overlay">
                        <div class="text">
                            <strong>MTA nucleosidase</strong> <br> PDB IDs : 2H8G, 3BSF <br> <em>PROTEINS</em> 65, 519-523(2006)
                        </div>
                    </div>
                </div>
                <!-- picture end -->
                <hr class="hr-line">
~~~

 1) 위의 코드 복붙하기(Indentation은 매우 중요하니 복붙할 때 다른 indentation과 맞춰줄것!!!)
 2) `<a href="여기에 pdf 주소 혹은 관련 사이트 url을 넣고"><img src="여기에 사진 주소를 넣을 것" alt="Avatar" class="image">`
 3) div class="text" 밑에 사진 내용, PDB ID, journal 적기.

4. Navigation 수정

- 추가 및 삭제

 data/navigation.yml에서

  - title: Members
  url: /members/
 
 를 추가 및 삭제.

이후 같은 이름의 폴더를 만들고, 폴더안에 index.md 생성


5. pdf
assets의 pdf폴더에 업로드

6. picture
assets의 img or gallery 폴더에 업로드

- 사진 규격 목록(cm)
~~~
   gallery 용 : 정해지지 않음

   Slide 용 : 폭 - 133.12, 높이 - 92.49, 해상도 - 300

   Member : 폭 - 1.08, 높이 - 1.44, 해상도 - 300
~~~

7. Posting

 1) -post에서 신규 포스트 만들 수 있음.
 - 주의 : 제목(title)은 반드시 영어로 적어야함. 띄어쓰기대신 -로 띄어쓰기
  ex)2018-06-30-ever-never.
