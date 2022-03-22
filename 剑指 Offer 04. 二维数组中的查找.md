# 第一次提交

## 代码

```c++
class Solution {
public:
    bool findNumberIn2DArray(vector<vector<int>>& matrix, int target) {
        if(matrix.size()==0) return false;
        if(matrix[0].size()==0) return false;
        int col=matrix[0].size()-1,row=0;
        while(col<matrix[0].size()&&col>=0&&row<matrix.size()&&row>=0)
        {
            if(target==matrix[row][col])
            {
                return true;
            }
            else if(target>matrix[row][col])
            {
                row++;
            }
            else
            {
                col--;
            }
        }
        return false;
    }
};
```

## 总结

- 两个方向都有单调性变化，可以使用二叉搜索树
- 注意特殊输入的处理