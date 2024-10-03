# QUIKSORT_RECURSSION
public class Main{
    public static void main(String []args){
        int []arr={0,9,8,7,4,5,6,7,8,6,5,4,3};
       sorter(arr.length-1,0,arr);
        System.out.println(Arrays.toString(arr));




    }
    static void sorter(int hi,int low,int []arr){
        if(low>=hi){
            return ;
        }

        int s=low;
        int e=hi;
        int piv=s+(e-s)/2;
        int mid=arr[piv];
        while(e>=s){
            while(arr[s]<mid){
                s++;
            }
            while(arr[e]>mid){
                e--;
            }
            if(s<=e){
                int temp=arr[s];
                arr[s]=arr[e];
                arr[e]=temp;
                s++;
                e--;
            }


        }
        sorter(e,low,arr);
        sorter(hi,s,arr);
    }
}

