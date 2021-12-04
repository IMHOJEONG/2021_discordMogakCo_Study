## 5 - 2021.1.1  - 5회차 

### 20:00 ~ 23:00

1. jintuna.com 도메인을 사서 추가함 

    - 화면 렌더링 속도에 문제가 있어
        - 자원들을 최적화할 수 있는 webpack을 추가할 가 생각중 

    - 아직 프로토타입만 작성했으며, 부족한 내용들은 부모님과 함께 상의하여 추가할 예정 

2. 알고리즘 sw expert academy
    - d3 문제 2개 풀이 

    - https://swexpertacademy.com/main/talk/solvingClub/problemView.do?solveclubId=AV6kld8aisgDFASb&contestProbId=AV14P0c6AAUCFAYi&probBoxId=AV-HZfeqN3ADFASP&type=PROBLEM&problemBoxTitle=%5BD2%7ED3+%EB%AC%B8%EC%A0%9C%ED%92%80%EC%9D%B4%5D+%EA%B8%B0%EC%B4%88+%EB%8B%A4%EC%A7%80%EA%B8%B0+Part3&problemBoxCnt=14

    ```java
    int test1 = sc.nextInt();
            sc.nextLine();
            String test = sc.nextLine();
             
            String check = sc.nextLine();
             
            int result = 1;
            int k = check.indexOf(test); 
            while( k !=-1 ){
                k = check.indexOf(test, k+1);
                if( k == -1) {
                    break;
                } 
                else {
                    result++;
                }
            }
             
             
            System.out.println("#"+test_case+" " + result);
    ```

    - s/w 문제해결 기본 sum
        - https://swexpertacademy.com/main/talk/solvingClub/problemView.do?solveclubId=AV6kld8aisgDFASb&contestProbId=AV13_BWKACUCFAYh&probBoxId=AV-HZfeqN3ADFASP&type=PROBLEM&problemBoxTitle=%5BD2%7ED3+%EB%AC%B8%EC%A0%9C%ED%92%80%EC%9D%B4%5D+%EA%B8%B0%EC%B4%88+%EB%8B%A4%EC%A7%80%EA%B8%B0+Part3&problemBoxCnt=14

        ```java
        int cases = sc.nextInt();
            int[][] test = new int[100][100];
             
            for(int i = 0 ; i < 100 ; i++) {
                for(int j = 0 ; j < 100 ; j++){
                    test[i][j] = sc.nextInt();
                }
            }
             
            int result = 0;
             
            for(int i = 0 ; i < 100 ; i++) {
                int check = 0; 
                  
                for(int j = 0 ; j < 100 ; j++){
                    check += test[i][j];
                }
                if(result < check){
                    result = check; 
                }   
            }  
             
            for(int i = 0 ; i < 100 ; i++) {
                int check = 0; 
                  
                for(int j = 0 ; j < 100 ; j++){
                    check += test[j][i];
                }
                if(result < check){
                    result = check; 
                }   
            }
             
            int check3 = 0; 
            for(int i = 0, j = 0 ; i < 100 ; i++, j++) {
                 
                    check3 += test[i][j]; 
                    
            }
             
            if(result < check3){
                result = check3;
            }
             
            int check4 =0;
             
            for(int i = 99, j = 0 ; i >= 0 && j < 100; i--, j++){
                    check4 += test[i][j]; 
            }
             
            if(result < check4){
                result = check4;
            }
             
            System.out.println("#"+test_case+" " + result);
        ``` 

- 정리 해야할 것 찾기