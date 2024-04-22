# sum-of-subarray
# 1


class Solution
{ static ArrayList<Integer> subarraySum(int[] arr, int n, int s) 
    {
       
        Map<Integer, ArrayList<?>> map=new LinkedHashMap();
        
        
        
        for( int i=0;i<n;i++)
        {
            if(arr[i]==s)
                {
                   
                    return new ArrayList<Integer>(Arrays.asList(i+1, i+1));
                }
                
                
            for(int j=i+1;j<n;j++)
            {
                
                int sum=0;
                List<Integer> sumlist = new ArrayList<>();

                for(int k=i;k<=j;k++)
                {
                    sum+=arr[k];
                }
                
                sumlist.add(i+1);
                sumlist.add(j+1);
                   
                    
                map.put(sum,new ArrayList<>(sumlist));
                if(sum==s)
                {
                   
                    return (ArrayList<Integer>) map.get(s);
                }
                
                
               
                 
            }
            
            
               
        }
      return new ArrayList<>(Arrays.asList(-1));
        
    }
}



# 2

