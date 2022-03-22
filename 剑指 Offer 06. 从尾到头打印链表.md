# 第一次提交

## 代码

```c++
class Solution {
public:
    vector<int> reversePrint(ListNode* head) {
        vector<int> result;
        while(head)
        {
            result.emplace_back(head->val);
            head=head->next;
        }
        reverse(result.begin(),result.end());
        return result;
    }
};
```

# 第二次提交

## 代码

```c++
class Solution {
public:
    vector<int> reversePrint(ListNode* head) {
        vector<int> result;
        dfs(result,head);
        return result;
    }
    void dfs(vector<int> &result,ListNode *head)
    {
        if(head==NULL)
            return;
        dfs(result,head->next);
        result.emplace_back(head->val);
    }
};
```

