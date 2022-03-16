# 代码

```c++
class Solution {
public:
    int findRepeatNumber(vector<int>& nums) {
        int position,n=nums.size();
        for(int i=0;i<nums.size();i++)
        {
            
            position=nums[i]%n;
            nums[position]+=n;
        }
        for(int i=0;i<nums.size();i++)
        {
            if(nums[i]>2*n)
                return i;
        }
        return 0;
    }
};
```

