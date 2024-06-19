class Solution {

    double maxVolume(double perimeter, double area) {
        // code here
        double l = (double)(perimeter - Math.sqrt(perimeter * perimeter - 24 * area)) / 12;
 
        double height = (perimeter / 4) - (2 * (l));
        
        double ans = l * l* height;
        return ans;
    }
}
