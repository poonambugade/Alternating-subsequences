# Alternating-subsequences
my code(python 3.6)
/*You are given an array of N non-negative integers: A1, A2, ..., AN. An alternating subsequence is a subsequence in which the indices of any two consecutive elements differ by exactly two in the original array. That is, if Ai1, Ai2, ..., Aik is some subsequence, then for it to be an alternating subsequence, (i2 - i1 = 2), (i3 - i2 = 2), and so on should all hold true. Among all alternating subsequences, find the one which has maximum sum of elements, and output that sum.*/

T=int(input())
for _ in range(T):
    n=int(input())
    a=list(map(int,input().split()))
    odd,even = 0,0
    for i in range(n):
        if i & 1:
            odd = odd + a[i]
        else:
            even = even + a[i]
    print(max(odd, even))
