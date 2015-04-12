# Recursive-binary-search-
This code will perform a recursive binary search of an array


 * @author Caboose1
 */
public class Project8 {

    
   
   
   private static int binarySearch(int[ ] array, int value,int start, int end) {
      if ((end - start) <= 1 ){
          if(array[start]== value)
              return start;
      if (array[end]== value)
          return end;
        return -1;
   }
      
   
   int midPoint = (start + end)/2;
   if(array[midPoint] > value) {
       return binarySearch(array,value,0,midPoint);
   }else{
       return binarySearch(array,value,midPoint,end);
   }
   
}
   



public static void main(String[] args) {
     int [] a = {4,9,10};
     System.out.println(binarySearch(a,20 ,0,a.length-1));
   }
}
