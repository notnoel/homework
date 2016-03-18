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

public static int Mode(int array[]) {
int max=0, count=0;
int length = array.length;
for (int i = 0; i <length; ++i) {
int count = 0;
for (int k = 0; k <length; ++k) {
if (array[k] == array[i]) ++count;
}
if (count > max)
{
max = count;
max = array[i];
}
}
return max;
}

public static int Median(int array[]) {
int length=array.length;
int[] middle = new int[length];
System.arraycopy(array, 0, middle, 0, middle.length);
Arrays.sort(middle);
if (length % 2 == 0) {
return (middle[(middle.length / 2) - 1] + middle[middle.length / 2]) / 2;
} else {
return middle[middle.length / 2];
}
}
