# Minimum-Time-Visiting-All-Points-using-Java-Leetcode

    import java.util.*;
    class Solution {
        public int toTime(int[] from, int[] to){
            return Math.max(Math.abs(from[0]-to[0]),Math.abs(from[1]-to[1]));
        }
        public int minTimeToVisitAllPoints(int[][] points) {
            int time =0;
            for(int i =1; i<points.length;i++){
                time+=toTime(points[i-1],points[i]);
            }
            return time; 
        }
    }
