#include<stdio.h>
int main()
{
	float basic_salary,hra_percent,da_percent,tax_percent;
	float hra, da, tax,gross_salary, net_monthly;
	int is_above_50k;
	
	printf("enter the basic salary: ");
	scanf("%f" ,&basic_salary);
	
	printf("enter hra%%: ");
	scanf("%f", &hra_percent);
	
	printf("enter da%%: ");
	scanf("%f", da_percent);
	
	printf("enter tax%%: ");
	scanf("%f", tax_percent);
	
	hra = basic_salary * (hra_percent / 100);
	da =  basic_salary * ( da_percent/100);
	tax = basic_salary * (tax_percent/100);
	gross_salary = basic_salary+hra+da-tax;
	
	is_above_50k=(gross_salary>50000);
	
	net_monthly= gross_salary/12;
	
	printf("\nhra = %.2f",hra);
	printf("\nda = %.2f",da);
	printf("\ntax = %.2f",tax);
	printf("\ngross salary = %.2f", gross_salary);
	printf("\ngross salary above 50000? %d",is_above_50k);
	printf("\nnet_monthly salary = %.2f\n",net_monthly);
	return 0;
}
