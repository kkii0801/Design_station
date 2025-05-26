프로젝트 이름 : Design_station <br />
사용된 도구 : PWA, JavaScript, GSAP, Swiper, HTML, CSS <br />
사용환경 : PC, Mobile <br />
:point_right: [Design_station](https://kkii0801.github.io/Design_station/)

***

## 주요 인터렉션 설명

1. 클릭하면 각 section으로 이동하는 메뉴 구현하기
2. 오른쪽 하단에 고정된 top 버튼 구현하기
3. form 태그 활용하기
4. PWA로 빌드하기

***

## 클릭하면 각 section으로 이동하는 메뉴 구현하기

### 동작 예시
<div align="center"><img src="https://github.com/kkii0801/Readme_files/blob/main/images_3/Design_menumove.gif?raw=true"></div>


### 코드 설명
#### JavaScript
```
```
***

## 오른쪽 하단에 고정된 top 버튼 구현하기

### 동작 예시
<div align="center"><img src="https://github.com/kkii0801/Readme_files/blob/main/images_3/Design_top.gif?raw=true"></div>

### 코드 설명
``` JavaScript
function controlMenu(n){
  gnbList.forEach(function(item, i){
    if(i == n){
      gnbList[i].classList.add("active");
    }
    else{
      gnbList[i].classList.remove("active");
    }
  });

  if(n != 0){
    menuArea.classList.add("fixed");
    btnTop.classList.add("active");
  }
  else{
    menuArea.classList.remove("fixed");
    btnTop.classList.remove("active");
  }
}

btnTop.addEventListener("click", function(e){
  e.preventDefault();

  gsap.to(window, { scrollTo: 0, duration: 0.4 });
})
```
***

## form 태그 활용하기

### 적용 예시
<div align="center"><img src="https://github.com/kkii0801/Readme_files/blob/main/images_3/Design_form.png?raw=true"></div>

### 코드 설명
#### HTML
``` HTML
<section id="contact">
  <div class="title">
    <h2>CONTACT US</h2>
    <p>다양한 경험과 노하우로 성공을 설계합니다.</p>
  </div>
  <div class="content">
    <form>
      <div class="form">
        <div class="form_inner">
          <div class="input_wrap">
            <input type="text" id="name" placeholder="YOUR NAME*" autocomplete="off">
            <input type="text" id="email" placeholder="YOUR EMAIL*" autocomplete="off">
            <input type="text" id="subject" placeholder="SUBJECT*" autocomplete="off">
          </div>
          <div class="text_wrap">
            <textarea placeholder="YOUR MESSAGE" autocomplete="off"></textarea>
          </div>
        </div>
        <div class="submit">
          <input type="submit" value="SEND MESSAGE">
        </div>
      </div>
    </form>
  </div>
</section>
```

#### CSS
``` CSS
input[type=text]::-webkit-input-placeholder {
	color: #bbb;
}
input[type=text]::-moz-placeholder {
	color: #bbb;
}
input[type=text]:-ms-input-placeholder {
	color: #bbb;
}
input[type=text]:-moz-placeholder {
	color: #bbb;
}
textarea::placeholder {
	color: #bbb;
}
input[type=text], textarea {
	font-family: "Roboto", "Noto Sans KR", sans-serif;
	font-size: 0.875em;
	font-weight: 500;
	border: none;
}
input[type=text] {
	padding: 0 10px 0 20px;
	height: 50px;
	border-radius: 5px;
}
textarea {
	padding: 20px 10px 0 20px;
	border-radius: 5px;
	resize: none;
}
input[type=submit] {
	height: 65px;
	font-family: "Roboto", "Noto Sans KR", sans-serif;
	font-size: 0.875em;
	font-weight: 500;
	background-color: rgba(38,157,210, .6);
	color: #fff;
	border: none;
	cursor: pointer;
	border-radius: 3px;
}
input[type=submit]:hover,
input[type=submit]:focus {
	background-color: #087eb2;
}
```
```
#contact .content .form {
	margin: 0 auto;
	margin-top: 78px;
	max-width: 940px;
}
#contact .content .form .form_inner {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-between;
}
#contact .content .form .input_wrap {
	width: calc((100% - 40px)/2);
}
#contact .content .form .input_wrap input {
	margin-top: 29px;
	width: 100%;
}
#contact .content .form .input_wrap input:first-child {
	margin-top: 0;
}
#contact .content .form .text_wrap {
	width: calc((100% - 40px)/2);
	height: 208px;
}
#contact .content .form .text_wrap textarea {
	width: 100%;
	height: 100%;
}
#contact .content .form .submit {
	margin-top: 45px;
	text-align: center;
}
#contact .content .form .submit input {
	width: 240px;
}

@media only screen and (max-width: 940px) {
	#contact .content .form {
		margin-top: 28px;
		padding: 0 16px;
	}
	#contact .content .form .input_wrap {
		width: 100%;
	}
	#contact .content .form .text_wrap {
		margin-top: 28px;
		width: 100%;
	}
}
@media only screen and (max-width: 460px) {
	#contact .content .form .input_wrap input {
		margin-top: 10px;
	}
	#contact .content .form .text_wrap {
		margin-top: 10px;
	}
	#contact .content .form .submit {
		margin-top: 20px;
	}
}
```

## PWA로 빌드하기

PWA로 빌드하는 방법은 [link](https://github.com/kkii0801/O_Kitchen?tab=readme-ov-file#pwa%EB%A1%9C-%EB%B9%8C%EB%93%9C%ED%95%98%EA%B8%B0)를 통해 참조할 수 있다.
