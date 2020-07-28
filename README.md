js에서 간단한 DOM의 사용을 공부했다. `new Date()`를 통해 활용해 볼 수 있는 것 을 찾아보다가 online tutorial에서 디자인을 가져와서 시계를 구현 해 보았다. 

<br>



```js
<script>
        window.onload = function(){

            const deg = 6;

            const hr = document.querySelector('#hr');
            const mn = document.querySelector('#mn');
            const sc = document.querySelector('#sc');

            setInterval(() => {
                
                let day = new Date();
                let hh = day.getHours() * 30;
                let mm = day.getMinutes() * deg;
                let ss = day.getSeconds() * deg;

                hr.style.transform = `rotateZ(${(hh)+(mm/12)}deg)`;
                mn.style.transform = `rotateZ(${mm}deg)`;
                sc.style.transform = `rotateZ(${ss}deg)`;
            })  
        }
    </script>

```

window 객체와 DOM 객체를 불어오는 과정을 활용해 보고 싶었다. 
로직은 간단한데 디자인이 너무 이뻣던것 같다ㅋㅋㅋ.  


[image:3301A164-C2D9-44A1-82D2-CAF5BBBD0433-586-0000C69FA61B55FD/스크린샷 2020-07-28 오후 12.52.03.png]
