# min-cost-of-ropes-greedy
class Solution
{
    public:
    //Function to return the minimum cost of connecting the ropes.
    long long minCost(long long arr[], long long n) {
        // Your code here
         priority_queue<long long , vector<long long> , greater<long long>>pq ; 
        
    for(long long  i = 0 ; i< n ; i++){
            pq.push(arr[i]) ; 
        }
        
        long long ans = 0 ; 
        
         while(pq.size()>1){
          long long r1 = pq.top() ; 
          pq.pop() ; 
          long long r2 = pq.top() ; 
          pq.pop() ; 
          long long r3 = r1+r2 ; 
          ans+= r3 ; 
          pq.push(r3) ; 
        }
        
        return ans ; 
    }
};
