

//大到小排序
int cmp(const int* a,const int* b){
    return *(const int*)b-*(const int*)a;
}

int lastStoneWeight(int* stones, int stonesSize){
    qsort(stones,stonesSize,sizeof(int),cmp);
    while(stonesSize!=1 && stones[1]!=0){ //若stonesSize==1 則不會判斷 stones[1]!=0 即跳出
        stones[0]=stones[0]-stones[1];
        stones[1]=0;
        qsort(stones,stonesSize,sizeof(int),cmp);
    }
    return stones[0];   
}
