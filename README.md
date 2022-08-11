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
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
2nd Project
import java.util.ArrayList;
import java.util.Comparator;
import java.util.NoSuchElementException;

public class Main {

    public static void main(String[] args) {
        
        ArrayList<Country> Countries=new ArrayList<Country>();
        
        //Countrycode,Countryname,capital,population,Continent
        
        Country coun1=new Country(1,"Japan","Tokyo",4000000,"Asia");
        Country coun2=new Country(2,"USA","DC",400000000,"America");
        
        
        City c1=new City(1,"Tokyo",100000);
        City c2=new City(1,"Osaka",10000);
        City c3=new City(1,"Nagoya",20000);
        
        City n1=new City(2,"NYC",4000000);
        City n2=new City(2,"LA",1000000);
        
        
        coun1.Cities.add(c1);
        coun1.Cities.add(c2);
        coun1.Cities.add(c3);
        
        coun2.Cities.add(n1);
        coun2.Cities.add(n2);
        
        Countries.add(coun1);
        Countries.add(coun2);
        
        Country Max2=Countries.stream().max(Comparator.comparingInt(Country::getpop)).orElseThrow(NoSuchElementException::new);
        
        System.out.println(Max2.Countryname);
    }

}
import java.util.ArrayList;
import java.util.List;

public class Country {
    int countrycode;
    String Countryname; 
    String Capital; 
    int Population;
    String Continent; 
    ArrayList<City> Cities=new ArrayList<City>();

    public Country(int code,String n,String c,int p,String con) {
        countrycode=code;
        Countryname=n; 
        Capital=c; 
        Population=p;
        Continent=con;
    }

    public int getpop() {
        return Population;
    }

}
