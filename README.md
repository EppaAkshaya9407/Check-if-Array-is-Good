# Check-if-Array-is-Good
class Solution:
    def isGood(self, nums: List[int]) -> bool:
        m=max(nums)
        n=len(nums)
        if n!=m+1:
            return False
        count=Counter(nums)
        for i in range(1,m):
            if count[i]!=1:
                return False
        if count[m]==2:
            return True
        else:
            return False
