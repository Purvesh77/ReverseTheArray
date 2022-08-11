# ReverseTheArray
public class ReverseArray {  
    public static void main(String[] args) {  
        String [] arr = new String [] {"Purvesh", "Patil", "LetsUpgrade", "JS", "Webdev"};  
        System.out.println("Original array is: ");  
        for (int i = 0; i < arr.length; i++) {  
            System.out.print(arr[i] + " ");  
        }  
        System.out.println();
        System.out.println();
        System.out.println("Array in reverse order is: ");   
        for (int i = arr.length-1; i >= 0; i--) {  
            System.out.print(arr[i] + " ");  
        }  
    }  
}
