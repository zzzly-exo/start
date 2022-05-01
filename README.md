# use stack to be a squeue
int main(){
    LinkStNode*L,*L1;
    InitStack(L);InitStack(L1);
    int i,n=8;
    char a[n]={"13847925"};
    char e,e1,e2;
    for(i=0;i<n;i++){
        Push(L,a[i]);

    }


   while(GetTop(L,e)==true)
   {
    Pop(L,e1);
    GetTop(L1,e2);
    while(GetTop(L1,e)==true&&e1>e2){
        Pop(L1,e2);
        Push(L,e2);
    }
    Push(L1,e1);

   }
   while(GetTop(L1,e)==true){
    Pop(L1,e1);
    Push(L,e1);

    }
    while(GetTop(L,e)==true){
        Pop(L,e);
        printf("%c",e);

    }

return 0;
}
