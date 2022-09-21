# -dd
记录每日。
int maxArea(int* height, int heightSize){
    int val,max;
    max=fmin(height[0],height[heightSize-1])*(heightSize-1);
    int head=0;
    int tail=heightSize-1;
    while(tail>head){
        if(height[head]<height[tail]){
            for(int tem=height[head];height[head]<=tem && head<heightSize;head++);//head<S 防止越界（关键）
            val=fmin(height[tail],height[head])*(tail-head);
            if(val>max) max=val;
        }
        else{
            for(int tem=height[tail];height[tail]<=tem && tail>0;tail--);//tail（同上）
            val=fmin(height[head],height[tail])*(tail-head);
            if(val>max) max=val;
        }
    }
    return max;
    

}
