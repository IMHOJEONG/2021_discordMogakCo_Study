## 1. 2020.12.28 - 1회차

1. Hackerrank 문제 해결하기 

    - 30 Days Of Code 진행 중(현재 9일차) 
        - https://www.hackerrank.com/challenges/30-recursion/problem
        - 문제 자체는 쉽지만, 꼬리 재귀 최적화로 어떻게 풀 수 있을까
        ```javascript
        function factorial(n) {
            if( n <= 1 ){
                return 1;
            }
            else {
                return n * factorial(n-1)
            }

        }
        ```
        - 이미 꼬리 재귀 최적화를 할 필요가 없는 건가 라는 생각이 듬 


    - Java Code 문제 풀이 
        - https://www.hackerrank.com/challenges/java-anagrams/problem
        - 오랜만에 java 문제 풀이라 헷갈리네, 라이브러리에 감사합시다 ㅋㅋ
        ```java
        static boolean isAnagram(String a, String b) {
        // Complete the function
            String[] arrA = a.toLowerCase().split("");
            String[] arrB = b.toLowerCase().split("");
            if(arrA.length != arrB.length){
                return false;
            }
            boolean isAnagram = true;
            for(int i = 0 ; i < arrA.length ; i++){
                String check = arrA[i];
                int countA = 0;
                int countB = 0; 
                for(int j = 0 ; j < arrA.length ; j++){
                    if(check.equals(arrA[j])){
                        countA++;
                    }      
                }
                for(int j = 0 ; j < arrB.length ; j++){
                    if(check.equals(arrB[j])){
                        countB++;
                    }
                }
                if(countA != countB){
                    isAnagram = false;
                    break;
                }
            }
            return isAnagram;
        }
        ``` 

    - Java Code 문제 풀이 2 
        - https://www.hackerrank.com/challenges/pattern-syntax-checker/problem?h_r=next-challenge&h_v=zen
        - 예외 처리의 기본을 물어봄 => 예외가 발생하면 그 밑에는 실행하지 않는다는 것을 이용 
        ```java
        import java.util.Scanner;
        import java.util.regex.*;

        public class Solution
        {
            public static void main(String[] args){
                Scanner in = new Scanner(System.in);
                int testCases = Integer.parseInt(in.nextLine());
                while(testCases>0){
                    String pattern = in.nextLine();
                    //Write your code
                    try {
                        Pattern p = Pattern.compile(pattern);
                        System.out.println("Valid");
                    } catch ( PatternSyntaxException e) {
                        System.out.println("Invalid");
                    } 
                    testCases--;
                }
            }
        }
        ```

2. 가게 홍보 페이지 작성 중 
    - 현재 기본 구성은 완료 => 음... 더 부족한 부분이나 원하시는 부분이 있으면 추가 예정 
    - https://github.com/IMHOJEONG/Store_Promotion_Page