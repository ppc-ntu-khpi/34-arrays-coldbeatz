# Практична робота "Масиви, вирази, керування виконанням програми"

## Завдання: Знайти в масиві число, яке повторюється найбільшу кількість разів

<details>
  <summary>find</summary>
  Знаходить в массиві число, яке повторюється найбільшу кількість разів
  
  ```java
/**
	 * Знаходить в массиві число, яке повторюється найбільшу кількість разів
	 * 
	 * @param arr массив
	 * @return Повертає число, яке в массиві повторюються найбільшу кількість разів
	 */
	public static int find(int[] arr) {
		Map<Integer, Integer> nums = new HashMap<>();
		for (int number : arr) {
			Integer i = nums.get(number);
			nums.put(number, i == null ? 1 : i+1);
		}
		
		int max = Collections.max(nums.values());
		for (Map.Entry<Integer, Integer> number : nums.entrySet()) {
			if (number.getValue() == max)
				return number.getKey();
		}
		return -1;
	}
  ```
  
</details>

Результат:
----

![Gitter](https://github.com/ppc-ntu-khpi/34-arrays-coldbeatz/blob/master/Screenshot_17.png)<br><br>
![Gitter](https://github.com/ppc-ntu-khpi/34-arrays-coldbeatz/blob/master/Screenshot_18.png)<br><br>
![Gitter](https://github.com/ppc-ntu-khpi/34-arrays-coldbeatz/blob/master/Screenshot_20.png)<br>
