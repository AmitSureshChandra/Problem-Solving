# Problem-Solving
1. Sharing some of code snippet while problem solving

Question Link : https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem

![image](https://user-images.githubusercontent.com/47358181/120741836-6c7b4300-c513-11eb-8cce-5665d99007af.png)

solution :
    
    if __name__ == '__main__':
        n = int(input())
        arr = map(int, input().split())
    unique_sorted_list = list(set(list(arr)))
    print(unique_sorted_list[-2])
    
    
2. Nested-list Problem

Question Link : https://www.hackerrank.com/challenges/nested-list/problem
![image](https://user-images.githubusercontent.com/47358181/120897692-173f4e80-c645-11eb-9af4-3bbde145dc5b.png)

    
    def sortName(prop):
        return prop['name']
        
    if __name__ == '__main__':
        data = []
        scores = []
        for _ in range(int(input())):
            name = input()
            score = float(input())
            data.append({
                'name' : name,
                'score' : score
            });
            scores.append(score);
            
        scores = list(set(scores))
        scores.sort()
        second_minimum = scores[1]
        
        names = filter(lambda x: True if x['score'] == second_minimum else False,data)
        names = sorted(names, key=sortName)
        for name in names:
            print(name['name'])
