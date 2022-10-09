# -dd
记录每日。
int pivotIndex(int* nums, int numsSize){
    int sum=0;
    int left=0;
    for(int i=0;i<numsSize;i++) sum+=nums[i];
    for(int i=0;i<numsSize;i++){
        if(sum-nums[i]==2*left)  return i;
        left+=nums[i];
    }
    return -1;
}
