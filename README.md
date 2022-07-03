class Solution:
    def findMedianSortedArrays(self, nums1: List[int], nums2: List[int]) -> float:
        m = len(nums1)
        n = len(nums2)
        for i in range(n):
            nums1.append(nums2[i])
        nums1.sort()
        l = 0 
        r = (m+n)-1
        mid = (l + r)//2
        if ((m+n)%2!= 0):
            k = nums1[mid]
        else:
            k = (nums1[mid] + nums1[mid + 1])/2
        return k
