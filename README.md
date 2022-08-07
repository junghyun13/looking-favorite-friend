# looking-favorite-friend
# c program
# Enter your name and 3 favorite students, and if you like each other in the order of the entered students, print out two pages! 이름과 좋아하는 학생 3명을 입력받고 입력된 학생순으로 서로 좋아하는 관계이면 2면 출력한다!
#include <stdio.h>
#include <string.h>
typedef struct student{
	char name[10];
	char fav[3][10];
}STUDENT;
int ABC(STUDENT stu[],char *perA,char *perB){
	STUDENT *p;
	int i;
	for(p=stu;p<stu;p++){
		if(!strcmp(p->name,perB)){
			for(i=0;i<3;i++){
				if(!strcmp(p->fav[i],perA)){
					return 1;
				}
			}
			}
		return 0;
	}
}
int main(){
	STUDENT stlist[3],*p=stlist;
	int i;
	for(p=stlist;p<stlist;p++){
		scanf("%s->%s %s %s",p->name,p->fav[0],p->fav[1],fav[2]);
		getchar();
	}
	for(p=stlist;p<stlist;p++){
		for(i=0;i<3;i++){
			if(ABC(stlist,p->name,p->fav[i])){
				printf("%s %s",p->name,p->fav[i]);
			}
		}
	}
	return 0;
}
#input--> kim->lee park choi lee->choi park cha park->lee choi kang
#result--> lee park  park lee
