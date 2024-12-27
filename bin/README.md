# solo-project
겨울방학 개인 프로젝트 공유

/* eslint-disable */
import React, {useState} from 'react';
import logo from './logo.svg';
import './App.css';

function App() {

  let [글제목, 글제목변경] = useState(['엄마 생일', '짱구 영화봤당', '냉삼 먹음']);
  let [하트, 하트변경] = useState(0);
  let [하트2, 하트변경2] = useState(0);
  let [하트3, 하트변경3] = useState(0);
  let [모달2, 모달변경2] = useState(false);
  let [모달, 모달변경] = useState(false);
  let [모달3, 모달변경3] = useState(false);
  let posts = '다빈이의 하루';

  // function 제목바꾸기(){
  //   var newArray = [...글제목];
  //   newArray[0] = '크리스마스';
  //   글제목변경(newArray);
  // }
  
  return (
    <div className="App">
      <div className="black-nav">
        <div> 다빈 Blog </div>
      </div>
      <div className="list">
        <h3 onClick={() => 모달변경(!모달)}>{글제목[0]} <span onClick ={ ()=>{하트변경(하트 + 1)} }>💙</span> {하트} </h3>
        <p>2024. 12. 25</p>
        <hr/>
      </div>
      <div className="list">
        <h3 onClick={() => 모달변경2(!모달2)}>{글제목[1]} <span onClick ={ ()=>{하트변경2(하트2 + 1)} }>💛</span> {하트2} </h3>
        <p>2024. 12. 26</p>
        <hr/>
      </div>
      <div className="list">
        <h3 onClick={() => 모달변경3(!모달3)}>{글제목[2]} <span onClick ={ ()=>{하트변경3(하트3 + 1)} }>♥️</span> {하트3} </h3>
        <p>2024. 12. 27</p>
        <hr/>
      </div>

      {모달 && <Modal1 />}
      {모달2 && <Modal2 />}
      {모달3 && <Modal3 />}

      

    </div>
  );
}

function Modal2(){
  return(
    <div className="modal">
        <h2>마라탕, 영화, 산책</h2>
        <p>2024. 12. 26</p>
        <p>집에 돌아와서 최세일 만나서 마라탕 조지고 짱구 영화 조지고 커피쿡에서 음료 사들고 산책조짐
        </p>
      </div>
  )
}

function Modal1(){
  return(
    <div className="modal">
        <h2>엄마 생일이자 크리스마스</h2>
        <p>2024. 12. 25</p>
        <p> 아침부터 잠실에서 케이크 픽업하고, 밥 와랄라 먹구 케이크 먹었당
        </p>
      </div>
  )
}

function Modal3(){
  return(
    <div className="modal">
        <h2>피시방과 냉삼</h2>
        <p>2024. 12. 27</p>
        <p> 일어나서 부대찌개 먹고 피시방에서 칼바람 조지고 집에와서 코딩하다가 저녁 냉삼 조짐
        </p>
      </div>
  )
}

export default App;
