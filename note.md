插入排序(insertion-sort)：

```go
func insertionSort(input []int) []int {
	if len(input) <= 1 {
		return input
	}

	for i, length := 1, len(input); i < length; i++ {
		current := input[i]
		j := i - 1
		for  j >= 0 {
			if input[j] <= current {
				break
			}
			input[j+1] = input[j]
			j--
		}
		input[j+1] = current
	}
	return input
}
```

24页

