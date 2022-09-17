# DevOpslab4
import java.util.*;
public class Binary_search {
	public static void main(String [] args)
	{
		int a[] = {78,95,92,43,56,10};
		int low = 0;
		int high = a.length - 1;
		int mid = (low + high) / 2;
		Scanner sc = new Scanner(System.in);
		int element = sc.nextInt();
		
		while(low <= high)
		{
			if(a[mid] > element)
			{
				high = mid - 1;
			}
			else if(a[mid] == element)
			{
				System.out.println("Found at: "+mid);
				break;
			}
			else if(a[mid] < element)
			{
				low = mid + 1;
			}
			mid = (low + high)/2;
		}
		if(low > high) {
			System.out.println("Element not found");
		}
		
		
	}

}
