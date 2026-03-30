Here are **Java DSA Templates** (Interview-Priority Order)
You can **memorize these** and reuse in most problems.
I ordered them based on **most asked in interviews**.

---

# ⭐ PRIORITY ORDER (memorize in this order)

1. Sliding Window
2. Two Pointers
3. HashMap / Frequency
4. Binary Search
5. Prefix Sum
6. Backtracking
7. DFS / BFS
8. Heap / Priority Queue
9. Monotonic Stack
10. DP basic

---

# 1️⃣ SLIDING WINDOW TEMPLATE (MOST ASKED)

Use when:

* subarray
* substring
* longest / smallest window

```java
public int slidingWindow(int[] arr) {
    int left = 0;
    int ans = 0;

    for (int right = 0; right < arr.length; right++) {

        // expand window
        // add arr[right]

        while (condition_breaks) {
            // shrink window
            // remove arr[left]
            left++;
        }

        ans = Math.max(ans, right - left + 1);
    }

    return ans;
}
```

---

# 2️⃣ TWO POINTER TEMPLATE

Use when:

* sorted array
* pair sum
* palindrome
* remove duplicates

```java
public void twoPointer(int[] arr) {

    int left = 0;
    int right = arr.length - 1;

    while (left < right) {

        if (condition) {
            left++;
        } else {
            right--;
        }
    }
}
```

---

# 3️⃣ HASHMAP FREQUENCY TEMPLATE

Use when:

* count frequency
* duplicates
* anagram
* subarray sum

```java
HashMap<Integer, Integer> map = new HashMap<>();

for (int num : arr) {
    map.put(num, map.getOrDefault(num, 0) + 1);
}
```

---

# 4️⃣ BINARY SEARCH TEMPLATE

MOST IMPORTANT

```java
public int binarySearch(int[] arr, int target) {

    int left = 0;
    int right = arr.length - 1;

    while (left <= right) {

        int mid = left + (right - left) / 2;

        if (arr[mid] == target)
            return mid;

        else if (arr[mid] < target)
            left = mid + 1;

        else
            right = mid - 1;
    }

    return -1;
}
```

---

# 5️⃣ PREFIX SUM TEMPLATE

Use when:

* subarray sum
* range queries

```java
int[] prefix = new int[n];

prefix[0] = arr[0];

for (int i = 1; i < n; i++)
    prefix[i] = prefix[i - 1] + arr[i];
```

Range sum:

```
sum(l,r) = prefix[r] - prefix[l-1]
```

---

# 6️⃣ BACKTRACKING TEMPLATE

Use when:

* permutations
* combinations
* subsets
* N queens

```java
public void backtrack(List<List<Integer>> res,
                      List<Integer> temp,
                      int[] nums,
                      int start) {

    res.add(new ArrayList<>(temp));

    for (int i = start; i < nums.length; i++) {

        temp.add(nums[i]);

        backtrack(res, temp, nums, i + 1);

        temp.remove(temp.size() - 1);
    }
}
```

---

# 7️⃣ DFS TEMPLATE

```java
void dfs(int node, boolean[] visited) {

    visited[node] = true;

    for (int nei : graph[node]) {

        if (!visited[nei])
            dfs(nei, visited);
    }
}
```

---

# 8️⃣ BFS TEMPLATE

```java
Queue<Integer> q = new LinkedList<>();
q.add(start);

while (!q.isEmpty()) {

    int node = q.poll();

    for (int nei : graph[node]) {
        q.add(nei);
    }
}
```

---

# 9️⃣ PRIORITY QUEUE TEMPLATE (HEAP)

Top K problems

```java
PriorityQueue<Integer> pq =
    new PriorityQueue<>();

pq.add(num);
pq.poll();
```

Max heap

```java
PriorityQueue<Integer> max =
 new PriorityQueue<>((a,b)->b-a);
```

---

# 🔟 MONOTONIC STACK TEMPLATE

Next greater element

```java
Stack<Integer> stack = new Stack<>();

for (int i = 0; i < n; i++) {

    while (!stack.isEmpty()
      && arr[stack.peek()] < arr[i]) {

        int idx = stack.pop();
    }

    stack.push(i);
}
```

---

# 1️⃣1️⃣ DP TEMPLATE

```java
int[] dp = new int[n];

dp[0] = base;

for (int i = 1; i < n; i++) {

    dp[i] = Math.max(
        dp[i-1],
        dp[i-2] + arr[i]
    );
}
```

---

# ⭐ INTERVIEW CHEAT SHEET

If problem says:

Longest substring → Sliding window
Pair sum sorted → Two pointer
Top K → Heap
Subarray sum → Prefix sum
Permutations → Backtracking
Graph → DFS/BFS
Sorted search → Binary search
Next greater → Monotonic stack

---

# ⭐ MOST IMPORTANT 5 (MEMORIZE FIRST)

Sliding window
Two pointer
Binary search
Backtracking
Heap

---

If you want I can also give:

* FAANG DSA patterns
* Leetcode mapping pattern wise
* 50 problems to memorize
* Java recursion templates
