## 2. 2020.12.30 - 3회차 

### 20:00 ~ 23:00

- sw expert academy 

    - 패턴 마디의 길이 

        - https://swexpertacademy.com/main/talk/solvingClub/problemView.do?solveclubId=AV6kld8aisgDFASb&contestProbId=AV5P1kNKAl8DFAUq&probBoxId=AV9oaSMa3DEDFAQc&type=PROBLEM&problemBoxTitle=%5BD1%7ED2+%EB%AC%B8%EC%A0%9C%ED%92%80%EC%9D%B4%5D+%EA%B8%B0%EC%B4%88+%EB%8B%A4%EC%A7%80%EA%B8%B0+Part2&problemBoxCnt=14
        
    - 시간 배열 

        - https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5PttaaAZIDFAUq&categoryId=AV5PttaaAZIDFAUq&categoryType=CODE

    ```java
    import java.util.Scanner;
    import java.io.FileInputStream;
    import java.time.LocalTime;
    import java.text.DateFormat;
    import java.text.SimpleDateFormat;
    import java.time.format.DateTimeFormatter;

    int hour = sc.nextInt();
    int minute = sc.nextInt();
    int hour2 = sc.nextInt();
    int minute2 = sc.nextInt();
    
    LocalTime test = LocalTime.of(hour, minute).plusHours(hour2);
    LocalTime test1 = test.plusMinutes(minute2);
    
    //System.out.println("#" + test_case +" " + (test1.getHour())+" "+test1.getMinute());
    
    String pattern = "h m";
    DateFormat dateFormat = new SimpleDateFormat(pattern);
    System.out.println("#" + test_case +" " + test1.format);(DateTimeFormatter.ofPattern(pattern)));

    ```

    - 파스칼의 삼각형 

        - https://swexpertacademy.com/main/talk/solvingClub/problemView.do?solveclubId=AV6kld8aisgDFASb&contestProbId=AV5P0-h6Ak4DFAUq&probBoxId=AV9oaSMa3DEDFAQc&type=PROBLEM&problemBoxTitle=%5BD1%7ED2+%EB%AC%B8%EC%A0%9C%ED%92%80%EC%9D%B4%5D+%EA%B8%B0%EC%B4%88+%EB%8B%A4%EC%A7%80%EA%B8%B0+Part2&problemBoxCnt=14

        ```java
        int test = sc.nextInt();
           
            int[][] check = new int[test][test];
            
            for(int i = 0; i < test ; i++){
            	check[i][0] = 1;	
            }
            
            for(int i = 1; i < test ; i++){
                for(int j = 1; j < test ; j++){
            		check[i][j] = check[i-1][j-1] + check[i-1][j];
                }
            }
            
            System.out.println("#"+test_case);

            for(int i = 0; i < test ; i++){
                for(int j = 0; j < test ; j++){
                    if(i >= j){
                    	System.out.print(check[i][j]+" ");
                    }
                   
                }
                System.out.println();
            }
        ```

    - 파리 퇴치 

        - https://swexpertacademy.com/main/talk/solvingClub/problemView.do?contestProbId=AV5PzOCKAigDFAUq&solveclubId=AV6kld8aisgDFASb&problemBoxTitle=%5BD1%7ED2+%EB%AC%B8%EC%A0%9C%ED%92%80%EC%9D%B4%5D+%EA%B8%B0%EC%B4%88+%EB%8B%A4%EC%A7%80%EA%B8%B0+Part2&problemBoxCnt=14&probBoxId=AV9oaSMa3DEDFAQc

        ```java
        int N = sc.nextInt();
        int M = sc.nextInt();
        int[][] test = new int[N][N];
            
        for(int i = 0 ; i < N ; i++){
            for(int j = 0 ; j < N ; j++){
                test[i][j] = sc.nextInt();
            }
        }
            
        int max = 0;
        int y = 0;
        for(int q = 0 ; q <= N-M ; q++){
                
            for(int q1 = 0 ; q1 <= N-M ; q1++){
                int result = 0;
                for(int i = q ; i < q+M ; i++){
                    for(int j = q1 ; j < q1+M ; j++){
                        result += test[i][j];     
                    }
                }
                //System.out.println(result);
                if(max < result){    
                    max = result;
                }
                
            }
                
                
        }
        
        System.out.println("#"+test_case+" "+max);

        ```

    - 지그재그 숫자

        - https://swexpertacademy.com/main/talk/solvingClub/problemView.do?solveclubId=AV6kld8aisgDFASb&contestProbId=AV5PxmBqAe8DFAUq&probBoxId=AV9oaSMa3DEDFAQc&type=PROBLEM&problemBoxTitle=%5BD1%7ED2+%EB%AC%B8%EC%A0%9C%ED%92%80%EC%9D%B4%5D+%EA%B8%B0%EC%B4%88+%EB%8B%A4%EC%A7%80%EA%B8%B0+Part2&problemBoxCnt=14
        
        ```java
            int test = sc.nextInt();
            int result = 0 ;
            for(int i = 1 ; i <= test ; i++){
            	if(i % 2 != 0){
                	result += i;
                }
                else {
                	result -= i;
                }
            }
            System.out.println("#"+test_case + " " +result);
        ```