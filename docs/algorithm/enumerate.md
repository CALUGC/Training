# 枚舉
枚舉是最直觀的演算法，將有可能的答案都搜過一遍，當然沒有頭緒的搜尋可能會得到龐大的複雜度，要根據題目的性質來降低複雜度。
## 回朔
枚舉有時能用遞迴實作，在遇到不可能的情形馬上回傳，這種方法就叫做回朔ㄊ。
## 特殊枚舉方式
* 二進位：利用二進位來表示集合內有哪些元素要用，進而枚舉所有元素子集，但受限於時間複雜度$O(2^n)$，集合的元素個數通常只有30個(甚至15個)。   
* 字典序：利用 `next_permutation` 或 `prev_permutation` 達到枚舉元素的先後順序。時間複雜度為$O(N!)$
## 折半枚舉
有時遇到複雜度$O(2^n)$的算法，在無法用其他方法降低複雜度，可以試著將元素切成兩半，降低 $n$，再用其他算法組合起來。