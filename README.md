# HashMap



import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;
import java.util.Set;

public class HMap {
    public static void main(String[] args) {
        HashMap<Integer, String> hmap = new HashMap<Integer, String>();
        hmap.put(12, "XX");
        hmap.put(17, "YY");
        hmap.put(2, "AB");
        hmap.put(20, "XXZY");
        Set set = hmap.entrySet();
        Iterator iter = set.iterator();
        while(iter.hasNext()) {
            Map.Entry mentry = (Map.Entry)iter.next();
            System.out.println("Key is : " +mentry.getKey() + ", Value :" + mentry.getValue());
            //System.out.println(mentry.getValue());
            
        }
        String var = hmap.get(2);
        System.out.println("Value at index 2 is : " +var);
        hmap.remove(2);
        System.out.println("Map key and value after removed");
        
        Set set2 = hmap.entrySet();
        Iterator iter1 = set2.iterator();
        while(iter1.hasNext()) {
            Map.Entry mentry1 = (Map.Entry)iter1.next();
            System.out.println("Key is : " +mentry1.getKey() + ", Value :" + mentry1.getValue());
        
            
    } 
        System.out.println("Set is now : " + hmap.containsKey(17));
        System.out.println("Set is now : " + hmap.containsValue("XX"));//contains key of
        System.out.println("Size is now : " + hmap.size());
        
        //clone
        HashMap<Integer, String> hmap1 = new HashMap<Integer, String>();
        hmap1.put(19, "XXY");
        hmap1.putAll(hmap);
        System.out.println(hmap1);
        
        hmap.clear();
        System.out.println("Set is now : " + hmap );
        
        
    
}
}
