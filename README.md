# __PHP 프로젝트(Photo-free-download)__

<p>
<img src="https://img.shields.io/badge/license-mit-green">
<img src="https://img.shields.io/github/issues/chahyoungseok/Photo-free-download">
<img src="https://img.shields.io/badge/XAMPP v7.3.27-FB7A24?style=flat-square&logo=XAMPP-SV&logoColor=white"/>
</p>


## 1. 프로젝트 소개
 > 사진을 공유하고 무료로 다운로드 받을 수 있는 php 웹페이지

## 2. 사이트의 전체적인 간략한 설명
 - 무료사진 다운로드 사이트입니다.
 - 사진에 대한 추천 수를 통해 포인트를 지급합니다.
 - 조회 수가 많은 사진이나 추천수가 가장 많은 사진을 메인에 게시합니다.
 - 따라서 한 유저는 하루에 하나의 사진에만 추천 가능합니다.
 - 또한 다운로드 횟수를 정확히 파악하고자 하루에 중복되는 사진을 다운로드 불가합니다.
 - 포인트가 1000점 이상이 되면 관리자로 등급 시킵니다.
 - 관리자는 하루가 끝날 때, 버튼을 통해 전체회원의 추천권한, 다운로드권한, 포인트 갱신을 합니다.

## 3. 간단한 설정
 - phpsitedb.sql을 phpadmin에 불러오시면 임시로 만든 유저의 데이터들을 기반으로 작동합니다.
 - localhost:3307,"root","",""phpsitedb 입니다.

## 4. 사이트의 기능
    1 비 로그인 상태
      - 회원가입 기능
      - 로그인 기능
      - 홈페이지 창에서 추천을 많이받은 사진, 조회 수가 높은 사진을 링크로 들어가 볼 수 있습니다.
      - 링크를 통해 들어갔을 때 위의 사진들의 간략한 정보만 열람 가능합니다.

    2 로그인 상태
      - 로그아웃 기능
      - 정보 수정기능 (아무것도 안쓰고 저장하면 기존의 값으로 저장되는 편리한 기능 구현했습니다.)
      - 내 사진관 기능 (내가 올린 사진들을 모아두는 나만의 사진관을 만들어놓았습니다.)
      - 내 사진관 기능에선 물론 해당 사진링크에 접속 가능합니다.
      - 사진 업로드 기능
      - 전체 사진 관람기능 (3개씩 사진과, 조횟수 ,다운횟수를 게시해놓았습니다.)
      - 해당 사진을 클릭하면 해당사진의 링크로 접속합니다.

    3. 사진에대한 상세기능
     - 제목, 추천 수, 사진 게시 아이디, 다운로드 횟수, 내용, 다운로드 버튼을 기본적으로 구현했습니다.
     - 댓글기능과 다른 사용자의 댓글에 추천하기(좋아요)를 할 수 있는 기능
     - 해당 사진을 추천하는 기능
     - 전체사진목록 버튼 구현
     - 해당 사진을 올린사람에게 친구추가를 할 수 있는 버튼 구현
     - 친구가 이미 되어 있다면 “이미 친구추가가 되어있다”라는 문구 띄웁니다.
     - 친구추가 안된 친구라도 그 사람의 게시물을 열람가능
     - 위의 기능은 Photo of (userid)를 누르면 가능

     4. 내가 올린사진일 때
      - 댓글 중 마음에 드는 댓글 고정하는 기능
      - 사진의 제목이나 내용을 수정할 수 있는 기능
      - 사진을 삭제하는 기능
      - 친구추가 버튼 숨김
        내가 올린사진이 아닐 때
      - 사진을 수정, 삭제하는 버튼 숨김
      - 고정하기 버튼 숨김

     5. 친구목록 기능
      - 현재 친구가 없다면 친구가 없다고 띄웁니다.
      - 친구를 추가한다면 친구삭제기능과 친구사진관 바로가기, 메시지 친구추가하기 버튼이 존재합니다.
      - 친구인 유저에게만 메시지로 소통가능합니다.
      - 메시지친구가 없다면 메시지 창 추가버튼으로 창 추가합니다.
      - 메시지창이 있는 친구라면 추가버튼대신 창으로 바로가기 버튼이 보입니다
      - 친구사진관 바로가기버튼을 누를시 해당 친구가 올린 게시물만 열람 가능합니다.

     6. 추천친구 기능
      - 친구목록에서 활용
      - 상대가 나에게 친추가 걸려있다면 추천친구 목록에 뜸
      - 상대가 나에게 친추가 안걸려있다면 추천친구 목록에 안뜸
      - 내가 상대에게 친추를 걸면 그 즉시 그 상대의 추천친구 목록에 내가 뜸
      - 내가 친구를 삭제했을 때 상대는 나에게 친추가 걸려있다면 내 추천친구목록에 뜸
      - 내가 친구를 삭제했을 때 상대가 나에게 친구가 안걸려있다면 친구의 추천목록에서 나를 지움
      - 추천친구가 없다면 추천친구가 없다고 뜸

     7. 메시지목록기능
      - 카카오톡의 UI를 모방했습니다.
      - 앞서 말했듯이 내가 친구로 추가시킨 유저에게만 메시지 창을 열 수 있습니다.
      - 메시지창이 추가되어있는 유저의 목록을 보여줍니다.
      - 해당유저를 클릭하면 그 유저와의 채팅창으로 접속하게 됩니다.
      - 채팅창에서 메시지 전송 가능합니다.
      - 친구목록에서도 해당 채팅창으로 바로이동 가능합니다.
      - 친구목록에서 친구삭제 하게 되면 해당 메시지창과 메시지 기록들이 삭제됩니다.

     8. 관리자 기능
      - Settle the day라는 버튼을 통해 하루가 끝날 때 전체회원의 추천권한, 다운로드 권한, 포인트 갱신을 합니다.
      - 본인의 사진이 아니더라도 수정, 삭제가 가능합니다.
      - 다만 고정하기 기능은 해당 사진을 올린 사용자가 아니면 관리자도 건들이지 못하는 기능으로 구현하였습니다.

 ## 5. 사진과 함께 소개
   1. 메인화면(로그아웃)
   <img src="/pictures/LogoutMain.PNG" width="500">
   2. 회원가입
   <img src="/pictures/Membership.PNG" width="500">
   3. 로그인
   <img src="/pictures/Login.PNG" width="500">
   4. 사진링크(로그아웃)
   <img src="/pictures/LogoutPhotoLink.PNG" width="500">
   5. 메인화면(로그인)
   <img src="/pictures/LoginMain.PNG" width="500">
   6. 정보수정
   <img src="/pictures/changInfo.PNG" width="500">
   7. 내 사진관
   <img src="/pictures/myPhotoList.PNG" width="500">
   8. 사진페이지(non-host)
   <img src="/pictures/PhotoDetail.PNG" width="500">
   <img src="/pictures/PhotoDetail2.PNG" width="500">
   9. 내 사진페이지(host)
   <img src="/pictures/myPhotoDetail.PNG" width="500">
   10. 사진수정 페이지(host)
   <img src="/pictures/photoModify.PNG" width="500">
   11. 사진업로드 페이지
   <img src="/pictures/photoUpload.PNG" width="500">
   12. 전체 사진관
   <img src="/pictures/PhotoList.PNG" width="500">
   <img src="/pictures/PhotoList2.PNG" width="500">
   13. 메시지 리스트
   <img src="/pictures/message.PNG" width="500">
   14. 대화 창 페이지
   <img src="/pictures/chatting.PNG" width="500">
   15. 친구 리스트
   <img src="/pictures/friendList.PNG" width="500">
   <img src="/pictures/friendList2.PNG" width="500">
   16. 친구 사진관
   <img src="/pictures/friendPhotoList.PNG" width="500">
   17. 관리자 메인화면
   <img src="/pictures/adminMain.PNG" width="500">
   18. 관리자 추가기능
   <img src="/pictures/adminFunction.PNG" width="500">
