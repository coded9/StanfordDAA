#Approach 1 --> Bruteforcing
```
import java.io.BufferedReader;
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;
import java.util.ArrayList;
import java.util.List;

public class InversionArrayCount{

	public static void main(String[] args) {
		List<Integer> list = new ArrayList<Integer>();
		File file = new File("C:/Users/coded9/Desktop/test.txt");
		BufferedReader reader = null;

		try {
		    reader = new BufferedReader(new FileReader(file));
		    String text = null;

		    while ((text = reader.readLine()) != null) {
		        list.add(Integer.parseInt(text));
		    }
		    long count = 0;
	        for(int i=0;i<list.size()-1;i++){
	            for(int j=i+1;j<list.size();j++){
	                if(list.get(i)>list.get(j)&&i<j){
	                    count++;
	                }
	            }
	        }
		
		//System.out.println(list);
		System.out.println(count); 

		} catch (FileNotFoundException e) {
		    e.printStackTrace();
		} catch (IOException e) {
		    e.printStackTrace();
		} finally {
		    try {
		        if (reader != null) {
		            reader.close();
		        }
		    } catch (IOException e) {
		    }
		}
		 
	}

}     #ANS:2407905288
```
