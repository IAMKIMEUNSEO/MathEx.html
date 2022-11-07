# MathEx.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- ★시험문제 출제★ -->
    <h2> 0~99 랜덤넘버 10개 발생</h2>
    <script>
        for (let i=0; i < 10; i++) {
            let rnum = Math.random() * 100;    
            //Math.random(): 0 <= x < 1보다 작은 랜덤 실수 리턴
            //Math.random() * 100: 0 <= x <100보다 작은 랜덤 실수 즉, 0~99.999
            let num = Math.floor(rnum);
            //Math.floor(m): m의 소숫점 이하 제거 정수 리턴
            //Math.floor(rnum): rnum의 소숫점 이하 제거 정수 즉, 0~99
            document.write(i + '번째 랜덤넘버는: ' + num + '<br>');
        }
    </script>



    <h2> 1~45 로또 랜덤넘버 발생 </h2>
    <script>
        for (let i=1; i<46; i++) {
            let lnum = Math.random() * 45      //0~45(0 <= x < 45)보다 작은 랜덤 실수 리턴
            let num = 1 + Math.floor(lnum);     // 1 + Math.floor(lnum): 1~45(1 <= x < 46)의 소숫점 이하 제거
            document.write(i + '번째 랜덤넘버는: ' + num + '<br>')
        }
    </script>



    <h2> 구구단 계산하기 </h2>
    <script>
        //1~9까지의 랜덤넘버 발생
        function randomInt () {
            return Math.floor(Math.random() * 9) + 1;
            //Math.random() * 9: 0~1 * 9 = 0~9(0 <= x < 9)보다 작은 실수
            //Math.floor(Math.random() * 9) + 1: 0~9 + 1 = 1~10(1 <= x < 10)보다 작은 정수
        }

        let gugudan = randomInt() + '*' + randomInt();     //ex) 5 * 8
        let userAns = prompt(gugudan + ' 값은 얼마일까요?');

        if (userAns == '') {
            document.write('구구단 연습을 종료하겠습니다.');
        }

        else {
            let ans = eval(gugudan);
            if (userAns == ans) {
                document.write("<strong>" + userAns + "</strong>" + '은' + ' 정답입니다.' + '<br>');
            }
            else {
                document.write("<strong>" + userAns + "</strong>" + '은' + ' 오답입니다.' + '<br>');
            }
            document.write('정답은' + gugudan + '=' + "<strong>" + ans + "</strong>");
        }
    </script>
</body>
</html>
