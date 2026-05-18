```C
void insertionSort(int arr[], int n)
{
	int key;
	for (int i = 0; i < n; i++)
	{
		key = arr[i]
		for (int j = i-1; j>=0 && arr[j]>key)
		{
			arr[j+1] = arr[j];
			j--;
		}
		a[j+1] = key;
	}
}
```
