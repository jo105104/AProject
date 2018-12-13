<template>
  <div id="uploadField" class="uploadField" style="height : 100%">
    <div class="explain">
      <div class="video">
        동영상 : 
        <input type="file" id="real-file" hidden="hidden" accept="video/*"/>
        <button type="button" id="custom-button" @click="onFileClick">동영상 파일</button>
        <span id="custom-text">No file chosen, yet.</span>
      </div>
      <hr>
      제목 <br> <input type="text" placeholder="제목"/><br><br>
      카테고리<br>
      <select>
        <option value="China">중식</option>
        <option value="Korea">한식</option>
        <option value="Pizza">피자</option>
      </select>
      <br><br>
      설명 <br> <textarea placeholder="동영상에대한 설명을 해주세요."/><br>
    </div>
  </div>
</template>

<style>
  hr {
    margin : 20px 0;
  }

  #custom-button {
    padding: 10px;
    color: white;
    background-color: #009578;
    border: 1px solid #000;
    border-radius: 5px;
    cursor: pointer;
  }

  #custom-button:hover {
    background-color: #00b28f;
  }

  .uploadField {
    background-color: rgba(223, 223, 223, 0.418);
    min-height: calc(100vh - 155px);
    display: -webkit-flex;
    display: flex;
  }

  #custom-text {
    margin-left: 10px;
    font-family: sans-serif;
    color: #aaa;
  }

  .explain {
    width : 40%;
    border : 1px solid black; 
    margin : 0 auto;
    margin-top: 20px;
    background-color: white;
    padding : 20px;
    height : 100%;
  }
</style>

<script>
  export default {
    name: 'uploadField',
    props: {
      msg: String,
      cnt: Number
    },
    methods : {
      onFileClick(){
        const realFileBtn = document.getElementById("real-file");
        const customBtn = document.getElementById("custom-button");
        const customTxt = document.getElementById("custom-text");
        event.stopPropagation();
        customBtn.addEventListener("click", function() {
          
          realFileBtn.click();
          console.log(1);
        });

        realFileBtn.addEventListener("change", function() {
          console.log(realFileBtn.value);
          if (realFileBtn.value) {
            customTxt.innerHTML = realFileBtn.value.split('\\').pop().split('/').pop();
          } 
        });
      }
    }
  }
</script>