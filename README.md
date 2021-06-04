# Problem-Solving
Sharing some of code snippet while problem solving

Question Link : https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem

![image](https://user-images.githubusercontent.com/47358181/120741836-6c7b4300-c513-11eb-8cce-5665d99007af.png)

solution :
    
    if __name__ == '__main__':
        n = int(input())
        arr = map(int, input().split())
    unique_sorted_list = list(set(list(arr)))
    print(unique_sorted_list[-2])
    
