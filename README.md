#任务one 
  <div id="box1">
                <button>全选</button>
                <button>不选</button>
                <button>反选</button>
              </div>
              <div id="box2">
                <ul>
                  <li>选项1：<input type="checkbox"></li>
                  <li>选项2：<input type="checkbox"></li>
                  <li>选项3：<input type="checkbox"></li>
                  <li>选项4：<input type="checkbox"></li>
                  <li>选项5：<input type="checkbox"></li>
                  <li>选项6：<input type="checkbox"></li>
                  <li>选项7：<input type="checkbox"></li>
                  <li>选项8：<input type="checkbox"></li>
                  <li>选项9：<input type="checkbox"></li>
           
                </ul>
              </div>
</body>
<script>
        window.onload = function(){
          // 获取所有的按钮
          var btns = document.getElementsByTagName("button");
          // 获取所有的选项input
          var inputs = document.getElementsByTagName("input");
   
          // 全选或者不选的时候 调用此函数
          function fun(flag){
            for (var i=0; i<inputs.length;i++) {
              inputs[i].checked = flag;
            }
          }
   
          //获取第一个按钮 “全选”
          btns[0].onclick = function(){
            fun(true);
          }
   
          // 获取第二个按钮 "不选"
          btns[1].onclick = function(){
            fun(false);
          }
          // 获取第三个按钮 “反选”
          btns[2].onclick = function(){
            // 遍历所有的选项，判断每一个选项是否被选中
            for (var i=0;i<inputs.length;i++) {
              inputs[i].checked == true ? inputs[i].checked = false : inputs[i].checked = true;
            }
          }
   
        }
      </script>



<style>
    .red {
        background-color: aquamarine;

    }

    .blue {

        background-color: blueviolet;
    }
</style>


<body>
    <input type="button" value="青色">
    <input type="button" value="紫色">




</body>
<script>

           var name = Gina;
           alert("The Face Thailand All Star winner Is"+name);



    window.onload = function () {
        var obtn = document.getElementsByTagName("input")[0];
        var obt1 = document.getElementsByTagName("input")[1];
        var otn = document.getElementById("xy");

      
        obt1.onclick= function(){
          document.body.className='blue'

        }

         obtn.onclick= function(){
          document.body.className='red'

        }
    }



</script>


</html>


   #shadow{
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background:orangered;
       /*设置透明度*/
        opacity: 0.5;
        filter: alpha(opacity=30);/*兼容IE*/
        display: none;
    }
    #obox{
        width: 300px;
        height: 300px;
        background: green ;
               /*物体绝对居中*/
        position: absolute;
        top: 50%;
        left: 50%;
        margin-top:-150px;
        margin-left: -150px;
        display: none;
    }
    </style>
</head>
<body>
    <input type="button" value="登录" id="obtn">
    <div id="shadow"></div>
    <div id="obox">
        <span id="os">x</span>
    </div>
</body>
<script>
    window.onload=function(){
        var oBtn=document.querySelector('#obtn');
        var oSw=document.querySelector('#shadow');
        var oBox=document.querySelector('#obox');
        var oS=document.querySelector('#os');
        oBtn.onclick=function(){
            oSw.style.display='block';
            oBox.style.display='block';
        }
        oS.onclick=function(){
            oSw.style.display='none';
            oBox.style.display='none';
        };
    }


   div div{
            width: 200px;
            height: 200px;
            border: 1px solid red;
            display: none;
        }

        .ys {
            background-color: darkmagenta;
        }
    </style>
</head>

<body>
    <div id="o1">
        <input type="button" class="ys" value="Team Lukkade">
        <input type="button"  value="Team Bee">
        <input type="button"  value="Team Cris">
        <div style="display: block">Team Lukkade></div>
        <div>Team Bee</div>
        <div>Team Cris</div>

    </div>

</body>
<script>
    function tab(Id) {
        var oBox = document.querySelector(Id);
        var aBtn = oBox.getElementsByTagName('input');
        var aDiv = oBox.getElementsByTagName('div');

        for (var i = 0; i < aBtn.length; i++) {
            aBtn[i].index = i;
            aBtn[i].onclick = function () {
                for (var i = 0; i < aBtn.length; i++) {
                    aBtn[i].className = '';
                    aDiv[i].style.display = "none";

                }
                 aDiv[this.index].style.display="block";
                 this.className='ys';

            }

        }
   }

      window.onload=function(){
            tab('#o1');

      }

</script>





</html>



