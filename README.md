import scala.collection.JavaConverters._

// you can write to stdout for debugging purposes, e.g.
// println("this is a debug message")

object Solution {
    def solution(n: Int): Int = {
    // write your code in Scala 2.12
    val s=n.toBinaryString
    var gap=0
    var counter=0
//    println(s)
    for(i <- s.toString)
    { 
     if (i.asDigit==1 && gap < counter)
       { gap=counter     
         counter=0
       } 
      if(i.asDigit==1)
        counter=0
       
     if (i.asDigit==0)
       counter=counter+1
    } 
    if(gap==1 && counter!=0)
    0
     else gap
  }

}



extremes 
n=1, n=5=101_2 and n=2147483647=2**31-1 ✔OK
▶ trailing_zeroes 
n=6=110_2 and n=328=101001000_2 ✘WRONG ANSWER 
got 3 expected 2
▶ power_of_2 
n=5=101_2, n=16=2**4 and n=1024=2**10 ✔OK
▶ simple1 
n=9=1001_2 and n=11=1011_2 ✔OK
▶ simple2 
n=19=10011 and n=42=101010_2 ✘WRONG ANSWER 
got 0 expected 1
▶ simple3 
n=1162=10010001010_2 and n=5=101_2 ✘WRONG ANSWER 
got 5 expected 3
▶ medium1 
n=51712=110010100000000_2 and n=20=10100_2 ✘WRONG ANSWER 
got 0 expected 1
1. 0.244 s OK
2. 0.232 s WRONG ANSWER,  got 0 expected 1
▶ medium2 
n=561892=10001001001011100100_2 and n=9=1001_2 ✘WRONG ANSWER 
got 7 expected 3
▶ medium3 
n=66561=10000010000000001_2 ✘WRONG ANSWER 
got 14 expected 9
1. 0.228 s WRONG ANSWER,  got 14 expected 9
▶ large1 
n=6291457=11000000000000000000001_2 ✔OK
1. 0.232 s OK
▶ large2 
n=74901729=100011101101110100011100001 ✘WRONG ANSWER 
got 9 expected 4
▶ large3 
n=805306373=110000000000000000000000000101_2 ✔OK
▶ large4 
n=1376796946=1010010000100000100000100010010_2 ✘WRONG ANSWER 
got 17 expected 5
▶ large5 
n=1073741825=1000000000000000000000000000001_2 ✔OK
▶ large6 
n=1610612737=1100000000000000000000000000001_2 ✔OK
