# sumoftwoArray 

package elclipse;

public class sumoftwoarray {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		int a[]= {1,8,2,7};
		int b[]= {2,3,8,6,7};

		int t[]=sum(a,b);
		print(t);	


	}

	public static void print(int[] arr) {            ////printing elements of the array
		for (int i = 0; i < arr.length; i++) {
			System.out.print(arr[i]+" ");
		}
		System.out.println();
	}

	public static int[] sum(int a[],int b[]) {

		int size=Math.max(a.length,b.length);   /////max of two array
		int sum[]= new int [size+1];
		int carry=0,t=0;
		int l1=a.length-1,l2=b.length-1,l3=sum.length-1;
		while(l3>=0) {
			if(l1>=0 && l2>=0) {
				sum[l3]=carry + a[l1] + b[l2];
				if(sum[l3]>9) {
					carry=1;
					sum[l3]%=10;
				}
				else {
					carry=0;
				}
				l1--;l2--;l3--;
			}
			else if(l1<0 && l2>=0 ) {
				sum[l3]=carry + b[l2];
				if(sum[l3]>9) {
					carry=1;
					sum[l3]%=10;
				}
				else {
					carry=0;
				}
				l2--;l3--;
			}
			else if(l1>=0 && l2<0) {
				sum[l3]=carry + a[l1];
				if(sum[l3]>9) {
					carry=1;
					sum[l3]%=10;
				}
				else {
					carry=0;
				}
				l1--;l3--;
			}
			else {
				sum[l3]=carry;
				l3--;

			}

		}



		return sum;            ////////////       return sum 

	}
}
