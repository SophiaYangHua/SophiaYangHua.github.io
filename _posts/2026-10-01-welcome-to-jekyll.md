---
title: "欢迎来到 Sophia Yanghua头脑风暴"
date: 2026-09-30 08:00:00 +0800
categories: [技术]
tags: [Jekyll, GitHub Pages, 博客搭建]
excerpt: "第一篇博客文章，聊聊为什么我要搭建这个技术博客，以及用 Jekyll + GitHub Pages 搭博客的踩坑记录。"
---

## 为什么建这个博客

说起来，想写博客的念头已经有很久了。

之前一直用各种笔记软件记录学习心得，但总觉得缺点什么。笔记是给自己看的，写的时候容易偷懒——逻辑跳几步、术语不解释、代码不跑通，反正自己能看懂就行。

但写博客不一样。一旦想着"别人可能会读"，就会逼着自己把事情想清楚、写明白。这就是所谓的**费曼学习法**吧——教别人，才是最好的学习方式。

> 输出是最好的输入。

所以就有了这个博客。不求有多少读者，只求每一篇文章都认认真真写，对得起点开链接的每一个人。

## 技术选型

选来选去，最终定了 **Jekyll + GitHub Pages** 的组合，原因很简单：

1. **纯静态**，不用管服务器和数据库
2. **GitHub Pages 原生支持**，push 就部署
3. **minima 主题**简洁干净，对中文和代码块都友好
4. **Markdown 写作**，专注内容本身

## 代码高亮示例

Jekyll 自带语法高亮（用的是 Rouge），支持几十种语言。下面放一段 Python 代码试试效果：

```python
# 一个简单的快速排序实现
def quicksort(arr):
    """对数组进行快速排序"""
    if len(arr) <= 1:
        return arr
    
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    
    return quicksort(left) + middle + quicksort(right)

# 测试
if __name__ == "__main__":
    numbers = [3, 6, 8, 10, 1, 2, 1]
    print(f"排序前: {numbers}")
    print(f"排序后: {quicksort(numbers)}")
```

再放一段 JavaScript：

```javascript
// 防抖函数
function debounce(func, wait) {
  let timeout;
  return function executedFunction(...args) {
    const later = () => {
      clearTimeout(timeout);
      func(...args);
    };
    clearTimeout(timeout);
    timeout = setTimeout(later, wait);
  };
}

// 使用示例
const handleSearch = debounce((query) => {
  console.log("搜索:", query);
}, 300);
```

语法高亮效果还不错吧？深色背景 + 彩色关键字，读代码舒服多了。

## 博客规划

接下来打算写这些方向的内容：

- **踩坑记录**：开发中遇到的问题和解决方案
- **技术笔记**：学习新技术时的整理和总结
- **项目实战**：做项目过程中的思考和经验
- **读书心得**：技术书籍的读书笔记

## 图片占位说明

下面是一个图片占位示例。以后写文章要插图的话，把图片放到 `assets/images/` 目录下，然后用 Markdown 语法引用就行。

![图片占位示例](/assets/images/example-placeholder.png)

*这里可以放图片，放在 assets/images/ 下引用*

## 小结

第一篇博客就写这么多。搭建过程比想象中顺利，Jekyll 的生态很成熟，GitHub Pages 的集成也很丝滑。

接下来就是坚持写了。万事开头难，开了头就不难了。
