# homework
Create a repository on GitHub for a Java program that finds the median (middle), mode (most common), and mean (average) for an array of integers. Create your program in such a way that you have a commit for the median method, a commit for the mode, and a commit for the mean. Submit a link to your repository on GitHub as your completion for this assignment.

public static int Mean(int array[]){
int sum = 0;
int average=0;
int length=array.length;
for(int i = 0; i < length; i++){
sum += array[i];
average = sum / length;
}
return average;
}
