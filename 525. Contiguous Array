//JavaScript 


const findMaxLength = (nums) => {
  const hash={};  //hashmap (key:count,value:index)
  let max_length=0,count=0;
  //遍歷陣列的每個數字  
  for (let i=0;i<nums.length;++i) {
    //count隨著遇到的數字做變化   
    if (nums[i]===0) count--;
    else count++;
    //根據count值，三種可能
    if (count===0) max_length=i+1; //case1:count為0 => 直接找到可能的長度，且一定是目前最大
    else{
        if (count in hash) max_length=Math.max(max_length,i-hash[count]); //case2:count在hash map有出現過 => 表示兩次同count的中間這段合為0
        else hash[count]=i; //case3:count在hash map沒出現過 => 登記進去
    }
  }
  return max_length;
};
