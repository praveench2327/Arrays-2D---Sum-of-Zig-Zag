# Arrays-2D---Sum-of-Zig-Zag
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
      Scanner s=new Scanner(System.in);
        int m=s.nextInt();
        int n=s.nextInt();
        int[][] a=new int[m][n];
        int i,j,sum=0;
        for(i=0;i<m;i++){
            for(j=0;j<n;j++){
                a[i][j]=s.nextInt();
            }
        }
    for(i=0;i<m;i++){
        sum+=a[0][i];
        sum+=a[m-1][i];
    }
    for(i=1;i<m-1;i++){
        sum=sum+a[i][m-i-1];
    }
    System.out.println("Sum of Zig-Zag pattern is "+sum);

    }
}
