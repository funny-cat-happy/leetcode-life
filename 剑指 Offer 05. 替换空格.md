# 代码

```c++
class Solution {
public:
    string replaceSpace(string s) {
        string h;
        for(int i=0;i<s.length();i++)
        {
            if(s[i]==' ')
            {
                h="";
                int j;
                for(j=0;j<i;j++)
                {
                    h+=s[j];
                }
                h+="%20";
                for(int k=j+1;k<s.length();k++)
                {
                    h+=s[k];
                }
                s=h;
                i+=2;
            }
        }
        return s;
    }
};
```

