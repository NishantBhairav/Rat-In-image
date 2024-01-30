# Rat-In-image
ADSA Project NISHANT BHAIRAV(21scse1010476)
import java.util.*;
public class mazepathBacktrack_no_03 {
    private static int count = 0;
    public static void findPossibleMazePath(int sr, int sc, int er, int ec, String s, boolean [][]isValid){
        if(sr< 0 || sc < 0) return;
        if(sr > er || sc > ec) return;
        
        if(isValid[sr][sc] == true) return;
        if(sr == er && sc == ec) {
            System.out.println(s);
            count++;
            return;
        }
        
        isValid[sr][sc] = true;
        // right 
        findPossibleMazePath(sr, sc+1, er, ec,  s + "R", isValid);
        // down 
        findPossibleMazePath(sr+1, sc, er, ec,  s+"D", isValid);
        //left
        findPossibleMazePath(sr, sc-1, er, ec,  s+"L", isValid);
import java.util.*;
public class mazepathBacktrack_no_03 {
    private static int count = 0;
    public static void findPossibleMazePath(int sr, int sc, int er, int ec, String s, boolean [][]isValid){
        if(sr< 0 || sc < 0) return;
        if(sr > er || sc > ec) return;
        
        if(isValid[sr][sc] == true) return;
        if(sr == er && sc == ec) {
            System.out.println(s);
            count++;
            return;
        }
        
        isValid[sr][sc] = true;
        // right 
        findPossibleMazePath(sr, sc+1, er, ec,  s + "R", isValid);
        // down 
        findPossibleMazePath(sr+1, sc, er, ec,  s+"D", isValid);
        //left
        findPossibleMazePath(sr, sc-1, er, ec,  s+"L", isValid);
