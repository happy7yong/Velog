<blockquote>
<p>🍀더도말고 덜도말고 <strong>하루에 한문제 코딩테스트 풀기!</strong>
플랫폼 : 프로그래머스
코테 푼 날짜 : 2025.01.15
문제 : OX 문제
Level 0</p>
</blockquote>
<h2 id="문제--ox-문제">문제 : OX 문제</h2>
<p><img alt="" src="https://velog.velcdn.com/images/happy7yong/post/181ba1e2-dc08-4349-a5df-c9befd05d19e/image.png" /></p>
<h2 id="제출답안">제출답안</h2>
<h3 id="javascript">javaScript</h3>
<pre><code class="language-jsx">function solution(quiz) {
    var answer=[]
    var quizStr=[]
    for(let num of quiz){
        quizStr=num.split(&quot; &quot;);
        for(let i=0;i&lt;quizStr.length;i+=2){
            quizStr[i]=parseInt(quizStr[i]);
        }

        if(quizStr[1]==&quot;+&quot;){
            if(quizStr[4]==quizStr[0]+quizStr[2]){
                answer.push(&quot;O&quot;);
            }else{
                answer.push(&quot;X&quot;);
            }
        }else if(quizStr[1]==&quot;-&quot;){
            if(quizStr[4]==quizStr[0]-quizStr[2]){
                answer.push(&quot;O&quot;);
            }else{
                answer.push(&quot;X&quot;);
            }
        }
    }
    return answer;
}</code></pre>
<br />
<hr />

<h2 id="⭐기억해야할-부분">⭐기억해야할 부분</h2>
<blockquote>
<p>🔵 <strong>헷갈리진 않았지만 효율적인 코드를 생각해내지 못했다.</strong>
중복코드가 많아서 압축시키고는 싶었으나... </p>
</blockquote>
<p>🔎 <strong>어떤 논리인가요?</strong></p>
<ol>
<li>문장을 배열로 분리하고</li>
<li>parseInt로 정수로 바꾼다.</li>
<li>1번에서 분리한 배열의 위치를 이용해 if문으로 산수 기호를 인식한다.</li>
<li>계산한다.</li>
</ol>
<br />

<h2 id="🖌️코드리뷰">🖌️코드리뷰</h2>
<p>중복코드가 많아서 아쉽다.</p>
<p>map()을 이용하면 더 품질좋은 코드를 짤 수 있을 것이다. 또한, map은 많은 코드에서 사용되기도 한다. 꼭 알아두어야할 메소드이다.</p>
<h3 id="🔎map">🔎map</h3>
<p>배열의 각 요소에 대해 주어진 함수를 호출하고, 새로운 배열값을 만드는 방법</p>
<p><strong>map(요소 =&gt; 변환하고 싶은 값)</strong></p>
<blockquote>
<p><strong>🔖숫자 배열 각 요소에 2을 곱하는 예제</strong>
doubled = numbers.map(num =&gt; num*2)</p>
</blockquote>
<pre><code>const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map(num =&gt; num * 2);

console.log(doubled); // [2, 4, 6, 8, 10]</code></pre><blockquote>
<p><strong>🔖객체 배열에 특정 요소만 추출하는 예제</strong>
names = users.map(user =&gt; user.name)</p>
</blockquote>
<pre><code>const users = [
    { name: 'Alice', age: 25 },
    { name: 'Bob', age: 30 },
    { name: 'Charlie', age: 35 }
];

const names = users.map(user =&gt; user.name);</code></pre>