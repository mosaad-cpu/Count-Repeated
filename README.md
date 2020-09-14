# Count-Repeated 

#include <stdio.h>

#include <stdlib.h>

int count_repated(int[],int);

int main (){


int arr[8]={5,3,2,2,5,2,5,3};


count_repated(arr,8);

return 0;

}

int count_repated(int arr[],int size){

int i =0 ,y =0;

int flag = -1, x = arr[y];

for(i=0;i<size+1;i++)

    {
    
   if((x - arr[i])==0)
   
      {
      
        flag++;
        
        arr[i]=0;
        
      }
      
  else if (i == size)
  
      {

      if (flag != 0 && x != 0)
      
        {
          printf("num:%d rep:%d\n",x,flag);
          
        }
        y++;
        
        x=arr[y];
        
        i=0;
        
        flag=-1;
        
      }
  else if(y==size)
  
      {
      
       break;
       
      }
      
}


}

