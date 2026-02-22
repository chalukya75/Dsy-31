# Dsy-31 Binary Gap
Data Scientist
class Solution {
    public int binaryGap(int n) {
        int last = -1, maxGap = 0, i = 0;
        while (n > 0) {
            if ((n & 1) != 0) {
                if (last != -1) {
                    maxGap = Math.max(maxGap, i - last);
                }
                last = i;
            }
            n >>= 1;
            i++;
        }
        return maxGap;
    }
}
