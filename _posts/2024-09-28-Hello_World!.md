---
layout: post
title: "Hello World!"
author: 'jinjehr'
date: 2024-09-28 20:25:00 +0900
last_modified_at: 2024-09-28 21:25:00 +0900
categories: [Github Blog, Jekyll]
tags: [github, jekyll, chirpy, blog]
img:
description: 처음
toc: true 
---

Hello World!

안녕하세요 블로그 첫 글입니다.

```테스트용 글입니다.``` 


<!-- 2024-07-28 글 작성 시작; 2024-08-29 페이지 호출 완료
<h2>Fitness-Calendar : 운동 일정 관리 웹 사이트</h2>
> - Tool :  
<img alt="React" src="https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=white" />
<img alt="VS Code" src="https://img.shields.io/badge/-Visual%20Studio%20Code-007ACC?style=flat-square&logo=visual-studio-code&logoColor=white" />

<br>

### 🔔 <a href="https://github.com/kim-src/fitness-calendar">Fitness-Calendar</a> 소개
### 📌 개발 동기
> - 운동 루틴을 관리할 수 있는 나만의 웹 애플리케이션을 개발하고 싶었습니다.
> - 이를 구현하기 위해, 또한 React 및 비즈니스 로직 학습을 위해 개발을 시작하였습니다.

### 📌 주요 기능
> - 달력에 개별 운동 루틴을 추가할 수 있습니다.
> - 운동 완료 현황을 알 수 있는 체크박스를 활용할 수 있습니다.
> - 운동 시간 체크를 위한 스톱워치/타이머를 이용할 수 있습니다.

### 📌 추후 개발 예정 내용
> - 운동 루틴을 운동 리스트로 관리할 수 있도록 설정하려고 합니다.
> - 운동 리스트에 운동 종목 추가 기능을 제공하려고 합니다.
> - 운동 리스트에 운동 종목 검색 기능을 제공하려고 합니다.
> - 개별 운동 종목과 관련된 유튜브 영상 재생 기능을 부여하려고 합니다.
> - <a href="https://github.com/kim-src/fitness-calendar">링크된 깃허브 레포지토리</a>를 클릭하시면 깃허브 레포지토리 페이지로 전환됩니다.

<figure>
    <img src="https://github.com/user-attachments/assets/d2b710d5-6b64-4a6d-b4bb-5225fae94c9b" class="img" alt="figure">
    <figcaption>개발중인 Fitness-Calendar</figcaption>
</figure>

<br>

### 🔔 개발 환경 설정
### 📌 React
> - Fitness-Calendar는 웹 프로그램으로 구현하였습니다.
> - JavaScript의 React 라이브러리를 선택한 이유는 컴포넌트 학습을 위해서입니다.
> - React는 재사용성이 좋은 UI 컴포넌트를 비교적 쉽게 관리할 수 있기 때문입니다.
> - React를 이용하기 가장 적합하다고 판단되는 IDE는 VS Code였습니다.

### 📌 IDE
> - Fitness-Calendar 개발을 위해 VS Code를 사용하였습니다.
> - VS Code는 다양한 테마와 플러그인으로 추가로 편리한 개발이 가능하기 때문입니다.
> - 또한 대중적인 IDE를 경험하고 싶었기 때문에 VS Code를 사용하였습니다.

### 📌 프로젝트 구조
> - React 프로젝트는 터미널에서 ```npx create-react-app``` 명령어로 생성하였습니다.
> - 이는 Node.js 패키지 실행 도구인 npx를 이용하여 React 프로젝트를 설치한 것입니다.
> - 기본적인 프로젝트 구조는 아래와 같습니다.
>    - public 디렉토리 : 메타 정보 등 브라우저에서 요구되는 파일이 포함됩니다.
>    - src 디렉토리 : React 프로젝트가 실질적으로 구동되는 파일이 포함됩니다.
>    - src/pages/MyCalendar.jsx : 뷰포트 페이지를 구성하는 컴포넌트를 포함합니다.
>    - src/components 디렉토리 : MyCalendar.jsx와 연결되는 컴포넌트를 포함합니다.
>    - src/assets 디렉토리 : CSS 및 글자 폰트 등의 파일을 포함합니다.
>    - src/index.js : 애플리케이션의 진입점이며 뷰포트에 표시될 컴포넌트를 선택합니다.

<br>

### 🔔 구현 과정 및 주요 기능
### 📌 메인 페이지(MyCalendar.jsx)
> - 브라우저 뷰포트에 표시될 내용을 포함시켰습니다.
> - 달력 라이브러리의 한 종류인 FullCalendar 라이브러리 코드를 작성하였습니다.
> - MyCalendar 컴포넌트에는 뷰포트에 표시될 최소한의 코드만을 포함시켰습니다.
> - MyCalendar 컴포넌트의 코드를 최소화하기 위해 컴포넌트를 분리시켰습니다.
> - 예를들면 운동 루틴 입력창, 스톱워치, 타이머 컴포넌트 등과 분리 및 연결시켰습니다.
> - 아래는 MyCalendar.jsx의 전체 코드입니다.

``` jsx
import dayGridPlugin from '@fullcalendar/daygrid'
import interactionPlugin from "@fullcalendar/interaction"
import FullCalendar from '@fullcalendar/react'
import React, { useRef, useState } from 'react'
import '../assets/css/calendar.css'
import '../assets/css/time-button.css'
import Editor from '../components/Editor'
import FitnessItem from '../components/FitnessItem'
import FitnessStopwatch from '../components/FitnessStopwatch'
import FitnessTimer from '../components/FitnessTimer'

function MyCalendar(props) {

    // const [상태 변수, 상태 업데이트 변수]
    // useState = contents 변수의를 빈 배열로 초기화
    // contents = 달력의 입력 이벤트를 할당하기 위해 사용
    // 배열 초기화 이유 = 최소 title 및 date 데이터를 할당시키기 위한 목적
    const [contents, setContents] = useState([]);
    // selectedDate = 선택된 날짜를 저장하는 상태 변수
    const [selectedDate, setSelectedDate] = useState(null);
    // showEditor = Editor 컴포넌트의 상태를 저장하는 상태 변수
    const [showEditor, setShowEditor] = useState(false);
    // showStopwatch = FitnessStopwatch 컴포넌트의 상태를 저장하는 상태 변수
    const [showStopwatch, setShowStopwatch] = useState(false);
    // showTimer = FitnessTimer 컴포넌트의 상태를 저장하는 상태 변수
    const [showTimer, setShowTimer] = useState(false);
    // id 부여를 위한 useRef 훅 사용
    const idRef = useRef(1);

    // arg = FullCalendar의 dateClick 이벤트 핸들러에서 전달되는 인자
    const addRoutine = (arg) => {
        // 달력 내부를 클릭하면 setShowEditor의 상태를 true로 변환
        setShowEditor(true);
        // 달력 내부를 클릭하면 클릭된 날짜를 setSelectedDate에 전달
        // arg.dateStr = FullCalendar 라이브러리에서 제공하는 arg 객체의 속성
        setSelectedDate(arg.dateStr);
    }

    // 비어있는 소괄호 = 실행될 예정이라는 의미
    const goFitnessTimer = () => {
        setShowTimer(true);
    }

    const goFitnessStopwatch = () => {
        setShowStopwatch(true);
    }

    // Editor.jsx에서 title이 입력될 경우 실행
    const saveRoutine = (title) => {
        if(title) {
            // newContent 객체를 contents 배열에 추가
            const newContent = {
                // id = idRef의 초기값인 1에서 1씩 값 증가
                id : idRef.current++,
                // title = 달력 내부에 표시되는 텍스트
                title : title,
                // date = 특정 날짜 지정
                date : selectedDate,
                // isDone = 운동 완료 상태 체크용 속성
                isDone : false
            };

            // 객체 상태 확인(디버깅)
            console.log("새로운 운동 루틴 :", newContent);

            // currentContents를 이용한 현재 상태 참조
            // newContent를 이벤트 목록에 추가하고 상태 업데이트
            // currentContents = contents 배열의 상태 참조 매개변수
            // newContent = title 및 date 데이터를 포함하는 이벤트 객체
            setContents(currentContents => [...currentContents, newContent]);
            // 내용 추가 후 Editor 컴포넌트 상태 false로 변경
            setShowEditor(false);
        }
    };

    // handleIsDone 함수에 전달된 인자 = event 객체의 id
    // 이벤트 핸들러 함수가 이벤트 발생 시 전달받는 event 객체의 id
    const handleIsDone = (id) => {
        // 업데이트 된 contents 상태에 접근
        // currentEvents.map = 모든 이벤트를 순회하며 특정 조건에 따른 업데이트 수행
        // map 함수 = 배열의 각 요소에 함수 실행 및 결과 반환 역할
        setContents(currentEvents => currentEvents.map(event =>
            // event 객체의 id와 함수에 전달된 id가 일치할 경우
            // event 객체의 isDone을 event 객체의 isDone이 아니게 설정
            // 즉, false 상태의 isDone을 true로 변환
            // 아니라면 event 객체 상태 유지
            event.id === id ? { ...event, isDone : !event.isDone } : event
        ));
    };

    // eventInfo = FullCalendar에서 제공하는 event 객체를 포함하는 객체
    // event 객체 = eventInfo 객체에 포함된 이벤트 객체
    // 객체의 구조-분해-할당 사용
    // eventInfo 객체에 포함된 event 객체 추출
    // event 객체에 포함된 id, title 등에 쉽게 접근 가능(필수 방식은 아님)
    const eventContent = ({event}) => {
        // extendedProps = FullCalendar 기본 속성이 아닌 커스텀 속성 포함
        // isDone 상태 확인을 위한 콘솔 출력
        // console.log("event.extendedProps 내용 :", event.extendedProps)

        return (
            // FitnessItem 호출
            <FitnessItem
                // FitnessItem 컴포넌트에 id 값 전달
                id={event.id}
                // FitnessItem 컴포넌트에 title 값 전달
                title={event.title}
                // event 객체의 extendedProps 속성의 isDone 속성값 전달
                isDone={event.extendedProps.isDone}
                // Toggle = 반전 기능 관련
                // handleIsDone 함수에 event 객체의 id 전달
                // parseInt = event.id를 정수로 변환하는 기능 제공
                // parseInt 사용으로 FullCalendar에서 이벤트 id를 문자열로 처리하는 문제 해결
                onToggle={() => handleIsDone(parseInt(event.id))}
            ></FitnessItem>
        );
    };

    return (
        <div>
            {/* 스톱워치 및 타이머 영역 */}
            <div className='time-button'>
                <button
                    className='stopwatch-button'
                    onClick={goFitnessStopwatch}
                >스톱워치</button>
                <button
                    className='timer-button'
                    onClick={goFitnessTimer}
                >타이머</button>
            </div>

            {/* Calendar Contents 영역 */}
            <FullCalendar
                // plugins = 사용할 플러그인 속성
                plugins={[ dayGridPlugin, interactionPlugin ]}
                // initialView = 달력 구성 속성
                initialView="dayGridMonth"
                // events = 상태 업데이트 관련 속성
                // contents = 달력 내부에 표시될 내용
                events={contents}
                // eventContent = FullCalendar의 커스텀 HTML 또는 React 컴포넌트 삽입을 위한 속성
                eventContent={eventContent}
                // dateClick = 달력 내부를 클릭했을 때 실행될 기능을 포함하는 속성
                dateClick={addRoutine}
                // button 텍스트 수정을 위한 속성
                buttonText={{ today : '이번달' }}
            ></FullCalendar>

            {/* showEditor의 상태가 true일 경우 Editor 컴포넌트 렌더링 */}
            {showEditor &&
                <Editor
                    // date prop = Editor 컴포넌트에 selectedDate 전달
                    date={selectedDate}
                    // onClose prop = 익명 함수로 setShowEditor 상태를 false로 설정
                    onClose={() => setShowEditor(false)}
                    // onSave prop = Editor 컴포넌트와 상호작용하여 데이터 수신
                    onSave={saveRoutine}
                ></Editor>
            }

            {/* showStopwatch의 상태가 true일 경우 FitnessStopwatch 컴포넌트 렌더링 */}
            {showStopwatch &&
                <FitnessStopwatch
                    // onClose prop = 익명 함수로 setShowTimer 상태를 false로 설정
                    onClose={() => setShowStopwatch(false)}
                ></FitnessStopwatch>
            }

            {/* showTimer의 상태가 true일 경우 FitnessTimer 컴포넌트 렌더링 */}
            {showTimer &&
                <FitnessTimer
                    // onClose prop = 익명 함수로 setShowTimer 상태를 false로 설정
                    onClose={() => setShowTimer(false)}
                ></FitnessTimer>
            }
        </div>
    )
}

export default MyCalendar;
```

### 📌 운동 루틴 입력 기능(Editor.jsx)
> - 운동 루틴을 추가할 수 있는 입력창 컴포넌트입니다.
> - MyCalendar 컴포넌트에서 달력의 날짜를 클릭하면 Editor 컴포넌트가 표시됩니다.
> - 렌더링 된 Editor 컴포넌트에는 클릭된 날짜와 글자 입력창 등이 포함됩니다.
> - 운동 루틴을 작성하고 Enter를 누르면 입력, ESC를 누르면 작업이 취소됩니다.
> - Editor 컴포넌트의 상태는 날짜 클릭 시 true, 닫기 버튼 클릭 시 false로 전환됩니다.
> - 아래는 Editor.jsx의 전체 코드입니다.

``` jsx
import React, { useState } from 'react';

// MyCalendar 컴포넌트로부터 전달되는 date, onClose, onSave props
// props (properties)= 부모 컴포넌트에서 자식 컴포넌트로 데이터를 전달할 때 사용
// props로 전달받은 데이터를 렌더링하는 과정 발생
function Editor({date, onClose, onSave}) {

    // 운동 내용 입력을 위한 useState 사용
    // title = FullCalendar의 내용 속성
    const [title, setTitle] = useState('');    

    // 저장 버튼 클릭 시 호출될 handleSave 함수 정의
    const handleSave = () => {
        // title의 상태를 onSave 함수에 전달
        onSave(title);
        // title 상태 전달 후 입력 필드 초기화
        setTitle('');
    }

    // 이벤트 발생 시 enterHandleSave 함수 실행
    const keyHandler = (e) => {
        // 엔터 입력 시 handleSave 함수 실행
        if(e.keyCode === 13) {
            handleSave();
        }
        if(e.keyCode === 27) {
            onClose();
        }
    }

    return (
        <div>
            <div>

            </div>
            <div
                style={{
                    // 상단으로부터 20%, 좌측으로부터 50% 위치에 고정
                    position : 'absolute',
                    top: '20%',
                    left: '50%',
                    // 컴포넌트의 너비에 상관없이 항상 중앙에 위치하도록 설정
                    transform: 'translateX(-50%)',
                    background: 'white',
                    padding: '20px',
                    boxShadow: '0 2px 7px rgba(0,0,0,0.7)',
                    // z-index 값 조정
                    zIndex: 1000
                }}
            >
                {/* MyCalendar 컴포넌트의 date */}
                <h2 style={{textAlign:'center'}}>{date}</h2>
                {/* 사용자에게 내용 입력 기능 제공 */}
                <input
                    type="text"
                    // 자동으로 포커스 설정
                    autoFocus
                    // value에 title 할당
                    value={title}
                    // e = 이벤트 정보가 담긴 객체
                    // e.target = 이벤트가 발생한 DOM 요소
                    // e.target.value = 입력 필드의 현재 값
                    onChange={(e) => setTitle(e.target.value)}
                    placeholder="운동 루틴을 입력하세요."
                    onKeyDown={keyHandler}
                ></input>
                {/* handleSave 함수에 데이터 저장 */}
                <button onClick={handleSave}>저장</button>
                {/* 에디터를 종료시키는 onClose 함수 호출 */}
                <button onClick={onClose}>취소</button>
            </div>
        </div>
    );
}

export default Editor;
```

<br>

### 🔔 스톱워치 기능(FitnessStopwatch.jsx)
### 📌 스톱워치 소개
> - MyCalendar 페이지 상단의 '스톱워치' 버튼을 클릭하면 스톱워치 창이 표시됩니다.
> - '시작' 버튼을 클릭하면 1초 단위로 시간이 증가됩니다.
> - '시작' 버튼을 클릭하면 버튼이 '정지' 버튼으로 변경됩니다.
> - '변경' 버튼을 클릭하면 시간 증가 작업이 정지됩니다.
> - '리셋' 버튼을 클릭하면 증가됐던 시간이 0으로 변환됩니다.

### 📌 스톱워치 기능 : isActive 변수
> - 스톱워치 컴포넌트의 초기 상태는 false이며 isActive 상태변수로 관리됩니다.
> - '시작' 버튼을 클릭하면 toggle 기능으로 상태변수의 상태가 반대로 설정됩니다.
> - 즉, '시작' 버튼을 클릭하면 false였던 isActive의 상태가 true로 전환됩니다.
> - 반대로 '정지' 버튼을 클릭하면 true였던 isActive의 상태가 false로 전환됩니다.
> - '시작' 또는 '정지' 버튼 변환 로직은 삼항연산자를 이용하였습니다.

### 📌 스톱워치 기능 : useEffect
> - 스톱워치를 구현하기 위한 숫자 계산 로직은 useEffect를 이용하였습니다.
> - useEffect는 컴포넌트 렌더링 후 부수적인 효과를 실행하기 위해 사용되는 편입니다.
> - useEffect가 의존하는 제어 요소는 isActive와 initialTime으로 설정하였습니다.
> - isActive가 true일 때, initialTime이 변경되며 스톱워치 작동 효과가 발현됩니다.
> - useEffect는 '시작' 버튼 클릭 후 isActive가 true일 때 실행됩니다.
> - '시작' 버튼으로 isActive의 상태가 true로 전환되면 useEffect가 실행됩니다.

### 📌 스톱워치 기능 : interval 변수 및 setInterval 함수
> - '시작' 버튼을 누르고 useEffect가 실행되면 interval 변수가 null로 초기화됩니다.
> - 그리고 isActive가 true이면 setInterval 함수로 initialTime이 증가됩니다.
> - initialTime은 1초마다 1씩 증가하도록 설정하였습니다.
> - '정지' 버튼을 누르면 isActive가 false로 전환됩니다.
> - isActive가 false이고 initialTime이 0이 아닌 경우 스톱워치는 정지됩니다.
> - 그리고 정지, 즉 증가되던 시간이 멈춘 상태를 return합니다.

### 📌 스톱워치 기능 : formatTime 함수
> - initialTime이 표시되는 형태를 formatTime 함수로 정의하였습니다.
> - initialTime은 기본적으로 '초' 단위의 숫자의 집합으로 설정하였습니다.
> - 따라서 스톱워치 역할을 부여하려면 initialTime을 시, 분, 초 단위로 환산해야 됩니다.
> - '시' 단위를 표현하기 위해 initialTime을 3600으로 나누었습니다.
> - '분' 단위를 표현하기 위해 '시' 단위로 나눈 것의 나머지에서 60을 나누었습니다.
> - '초' 단위를 표현하기 위해 initialTime을 60으로 나눈 것의 나머지를 구하였습니다.
> - 예를들어 initialTime이 3700일 경우 1, 1, 40이 되며 01:01:40으로 표현됩니다.
> - 참고로 Math.floor 함수는 '몫' 계산을 위한 것이며 소수점 없이 산출합니다.
> - 아래는 시간 계산에 대한 상세 내용입니다.

```
- '시' 계산 = 3700/3600 = 1.027... → 시 = 1
- '분' 계산 = 3700/3600 = 1.027... → (몫 = 3600 * 1 = 3600) → 나머지 = 3700 - 3600 = 100 → 100/60 = 1.666... → 분 = 1
- '초' 계산 = 3700/60 = 61.666... → (몫 = 60 * 61 = 3660) → 나머지 = 3700 - 3660 = 40 → 초 = 40
```

### 📌 스톱워치 기능 : hours, minutes, seconds 변수
> - hours, minutes, seconds 변수에 할당된 값을 디지털 시계 형태로 표현하였습니다.
> - hours, minutes, seconds 요소는 Fragment에 포함시켜 return하였습니다.
> - toString 메서드를 이용하여 각 요소를 문자열 형태로 변환하였습니다.
> - padStart 메서드를 이용하여 문자열을 기본적으로 두 자리수로 나타내었습니다.
> - 표시되는 값은 기본적으로 '00'으로 설정하였습니다.
> - 각 요소는 join 대신 span 태그를 이용하여 구분하였습니다.
> - 참고로 padStart 메서드는 문자열의 시작 부분을 특정 문자로 채우는 기능을 제공합니다.

### 📌 Fragment 태그
> - div 태그 대신 Fragment 태그를 사용한 이유는 DOM 요소를 생성하지 않기 때문입니다.
> - Fragment의 장점은 DOM 요소를 생성하지 않고 자식 요소를 그룹화할 수 있다는 것입니다.
> - DOM 요소를 미리 생성하지 않으면 렌더링 또는 업데이트 속도가 더 빨라집니다.
> - 참고로 Fragment 태그만 DOM 요소로 생성되지 않을뿐, 자식 요소는 DOM 요소로 생성됩니다.
> - 아래는 스톱워치 컴포넌트의 렌더링 모습 및 FitnessStopwatch.jsx의 전체 코드입니다.

<figure>
    <img src="https://github.com/user-attachments/assets/7edf6eae-a361-4cff-ba7c-595fcb4f6e18" class="img" alt="figure">
    <figcaption>스톱워치 기능 실행창 모습</figcaption>
</figure>

``` jsx
import React, { Fragment, useEffect, useState } from 'react';
import '../assets/css/fitness-stopwatch.css'

function FitnessStopwatch({onClose}) {
    
    const [initialTime, setInitialTime] = useState(0);
    const [isActive, setIsActive] = useState(false);

    // reset 함수 정의
    const reset = () => {
        // deliveredTime 초기화
        setInitialTime(0);
        // isActive 상태를 false로 전환
        setIsActive(false);
    };

    // toggle 함수 정의
    const toggle = () => {
        // 현재의 isActive 상태와 반대로 전환
        // 예를들어 현재 false인 경우 true로 전환
        setIsActive(!isActive);
    };

    // useEffect = 부수 효과(side effects) 수행 목적
    // 컴포넌트의 렌더링이 완료된 후 실행
    // 종속성 배열에 따라 실행 조건이 결정되는 것이 특징
    // 예를들면, 의존성을 부여한 것의 상태가 변경되면 실행
    useEffect(() => {
        // interval의 초기값을 null로 설정
        let interval = null;
        // 스톱워치를 실행하고 싶을 경우
        if(isActive) {
            interval = setInterval(() => {
                setInitialTime(initialTime => initialTime + 1);
            }, 1000);
        // 스톱워치 실행을 중지하고 싶을 경우
        } else if(!isActive && initialTime !== 0) {
            clearInterval(interval);
        }
        return () => clearInterval(interval);
        // isActive, initialTime 의존성 부여
        // isActive의 상태가 true에서 false로 전환 시 실행 중지
        // initialTime 값이 변경되면 useEffect 재실행
    }, [isActive, initialTime]);

    /* 스톱워치 숫자 표시 형식 */
    function formatTime(initialTime) {
        const hours = Math.floor(initialTime / 3600);
        // %로 나머지 계산
        const minutes = Math.floor((initialTime % 3600) / 60);
        // %로 나머지 계산
        const seconds = initialTime % 60;
    
        // 변수 선언을 최소화하기 위해 join 제외
        return (
            <Fragment>
                <div>{hours.toString().padStart(2, '0')}</div>
                <span className='colon'>:</span>
                <div>{minutes.toString().padStart(2, '0')}</div>
                <span className='colon'>:</span>
                <div>{seconds.toString().padStart(2, '0')}</div>
            </Fragment>
        )
    };
    
    return (
        <div>
            <div
                style={{
                    // 상단으로부터 20%, 좌측으로부터 50% 위치에 고정
                    position : 'absolute',
                    top: '20%',
                    left: '50%',
                    // 컴포넌트의 너비에 상관없이 항상 중앙에 위치하도록 설정
                    transform: 'translateX(-50%)',
                    background: 'white',
                    padding: '20px',
                    boxShadow: '0 2px 7px rgba(0,0,0,0.7)',
                    // z-index 값 조정
                    zIndex: 1000
                }}
            >
                {/* 스톱워치 설정 영역 */}
                <div style={{display:'flex', justifyContent:'center'}}>
                    <button onClick={toggle}>{isActive ? '정지' : '시작'}</button>
                </div>

                <br/>

                {/* 스톱워치 표시 영역 */}
                <div className='stopwatchMain' style={{display:'flex', justifyContent:'center'}}>
                    <div
                        className='stopwatchDisplay'
                        style={{
                            width: '1200px',
                            height: '200px',
                            borderRadius: '10px',
                            border: '1px solid black',
                        }}
                    >
                        {formatTime(initialTime)}
                    </div>
                </div>

                <br/>

                {/* 스톱워치 footer 영역 */}
                <div style={{display:'flex', justifyContent:'flex-end'}}>
                    <button onClick={reset}>리셋</button>
                    <span style={{marginRight:'15px'}}/>
                    <button onClick={onClose}>닫기</button>
                </div>
            </div>
        </div>
    );
}

export default FitnessStopwatch;
```

<br>

### 🔔 타이머 기능(FitnessTimer.jsx)
### 📌 타이머 소개
> - MyCalendar 페이지 상단의 '타이머' 버튼을 클릭하면 타이머 창이 표시됩니다.
> - 숫자 입력창에 원하는 타이머 시간을 입력하면 '시, 분, 초' 단위로 자동 환산됩니다.
> - 시간 입력 후 '타이머 설정' 버튼을 클릭하면 타이머 시간이 업데이트됩니다.
> - '시작' 버튼을 클릭하면 타이머 시간이 감소되며 기능이 작동됩니다.
> - '정지' 버튼을 클릭하면 타이머 기능이 정지됩니다.
> - '리셋' 버튼을 클릭하면 '타이머 설정' 버튼으로 설정했던 초기 시간으로 설정됩니다.
> - '닫기' 버튼을 클릭하면 타이머 창이 소멸됩니다.

### 📌 타이머 기능 : isActive 변수
> - 타이머 컴포넌트의 초기 상태는 false이며 isActive 상태변수로 관리됩니다.
> - '시작' 버튼을 클릭하면 toggle 기능으로 상태변수의 상태가 반대로 설정됩니다.
> - 즉, '시작' 버튼을 클릭하면 false였던 isActive의 상태가 true로 전환됩니다.
> - 반대로 '정지' 버튼을 클릭하면 true였던 isActive의 상태가 false로 전환됩니다.
> - '시작' 또는 '정지' 버튼 변환 로직은 삼항연산자를 이용하였습니다.

### 📌 타이머 기능 : useEffect
> - 타이머를 구현하기 위한 숫자 계산 로직은 useEffect를 이용하였습니다.
> - useEffect는 컴포넌트 렌더링 후 부수적인 효과를 실행하기 위해 사용되는 편입니다.
> - useEffect가 의존하는 제어 요소는 isActive와 initialTime으로 설정하였습니다.
> - isActive가 true일 때, initialTime이 변경되며 스톱워치 작동 효과가 발현됩니다.
> - useEffect는 '시작' 버튼 클릭 후 isActive가 true일 때 실행됩니다.
> - '시작' 버튼으로 isActive의 상태가 true로 전환되면 useEffect가 실행됩니다.

### 📌 타이머 기능 : deliveredTime 변수 및 setDeliveredTime 함수
> - '타이머 설정' 버튼을 클릭했을 때 초기 시간이 변경되는 효과를 부여하고 싶었습니다.
> - 이를 위해서 initialTime 변수 이외에도 시간을 표현할 수 있는 변수를 추가하였습니다.
> - 이는 deliveredTime 변수이며 이 변수는 initialTime에 할당된 값을 전달받습니다.
> - 타이머 숫자 입력란에 숫자를 입력하면 initialTime 변수에 값이 할당됩니다.
> - '타이머 설정' 버튼을 클릭하면 initialTime에 할당된 값이 deliveredTime에 전달됩니다.

### 📌 타이머 기능 : formatTime 함수
> - 타이머에 표시되는 시간은 deliveredTime이 '시, 분, 초' 단위로 환산된 값입니다.
> - deliveredTime에 할당된 값은 formatTime 함수로 인해 시간으로 표현됩니다.
> - 아래는 '시, 분, 초' 단위에 대한 설명이며 이는 스톱워치와 동일합니다.
> - '시' 단위를 표현하기 위해 initialTime을 3600으로 나누었습니다.
> - '분' 단위를 표현하기 위해 '시' 단위로 나눈 것의 나머지에서 60을 나누었습니다.
> - '초' 단위를 표현하기 위해 initialTime을 60으로 나눈 것의 나머지를 구하였습니다.
> - 예를들어 deliveredTime이 3700일 경우 1, 1, 40이 되며 01:01:40으로 표현됩니다.
> - 참고로 Math.floor 함수는 '몫' 계산을 위한 것이며 소수점 없이 산출합니다.
> - 아래는 시간 계산에 대한 상세 내용입니다.

```
- '시' 계산 = 3700/3600 = 1.027... → 시 = 1
- '분' 계산 = 3700/3600 = 1.027... → (몫 = 3600 * 1 = 3600) → 나머지 = 3700 - 3600 = 100 → 100/60 = 1.666... → 분 = 1
- '초' 계산 = 3700/60 = 61.666... → (몫 = 60 * 61 = 3660) → 나머지 = 3700 - 3660 = 40 → 초 = 40
```

### 📌 타이머 기능 : interval 변수 및 setInterval 함수
> - '시작' 버튼을 누르고 useEffect가 실행되면 interval 변수가 null로 초기화됩니다.
> - 그리고 isActive가 true이면 setInterval 함수로 deliveredTime이 감소됩니다.
> - initialTime은 1초마다 1씩 증가하도록 설정하였습니다.
> - '정지' 버튼을 누르면 isActive가 false로 전환됩니다.
> - isActive가 false이고 initialTime이 0이 아닌 경우 스톱워치는 정지됩니다.
> - 그리고 정지, 즉 증가되던 시간이 멈춘 상태를 return합니다.

### 📌 타이머 기능 : hours, minutes, seconds 변수
> - hours, minutes, seconds 변수에 할당된 값을 디지털 시계 형태로 표현하였습니다.
> - hours, minutes, seconds 요소는 Fragment에 포함시켜 return하였습니다.
> - toString 메서드를 이용하여 각 요소를 문자열 형태로 변환하였습니다.
> - padStart 메서드를 이용하여 문자열을 기본적으로 두 자리수로 나타내었습니다.
> - 표시되는 값은 기본적으로 '00'으로 설정하였습니다.
> - 각 요소는 join 대신 span 태그를 이용하여 구분하였습니다.
> - 참고로 padStart 메서드는 문자열의 시작 부분을 특정 문자로 채우는 기능을 제공합니다.

### 📌 타이머 기능 : displayTime 변수 및 setDisplayTime 함수
> - 타이머 설정 과정에서 입력한 숫자가 시간으로 환산되는 효과를 부여하고 싶었습니다.
> - 이를 displayTime 변수를 이용하여 구현하였으며 작동 방식은 아래와 같습니다.
>    - totalSeconds 변수에 숫자 입력란으로부터 입력된 값 할당(10진수)
>    - '시, 분, 초' 단위로 환산된 각각의 값을 toString으로 변환
>    - setDisplayTime 함수를 이용하여 입력된 값을 key-value 형태로 할당
>    - 각각의 key-value 쌍을 환산된 값에 맞게 렌더링 된 페이지에 표시

### 📌 Fragment 태그
> - div 태그 대신 Fragment 태그를 사용한 이유는 DOM 요소를 생성하지 않기 때문입니다.
> - Fragment의 장점은 DOM 요소를 생성하지 않고 자식 요소를 그룹화할 수 있다는 것입니다.
> - DOM 요소를 미리 생성하지 않으면 렌더링 또는 업데이트 속도가 더 빨라집니다.
> - 참고로 Fragment 태그만 DOM 요소로 생성되지 않을뿐, 자식 요소는 DOM 요소로 생성됩니다.
> - 아래는 스톱워치 컴포넌트의 렌더링 모습 및 FitnessTimer.jsx의 전체 코드입니다.

<figure>
    <img src="https://github.com/user-attachments/assets/46fbe2e0-aea6-4cfc-bfee-3d5eccc462f6" class="img" alt="figure">
    <figcaption>타이머 기능 실행창 모습</figcaption>
</figure>

<br>

### 🔔 추후 개발 예정 내용
### 📌 운동 루틴 관리 방식 업데이트
> - 운동 루틴에 대한 리스트를 생성하고 데이터베이스를 이용하여 관리하려고 합니다.
> - 저장된 운동 루틴을 검색 및 추가 기능을 제공하려고 합니다.
> - 운동 리스트에 관련 운동 방법과 관련된 유튜브 영상 재생 기능을 제공하려고 합니다.

<br>
<br>
<br> -->
