# codility
binary

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
       { gap=gap+counter
       counter=0}
     if (i.asDigit==0)
       counter=counter+1
    //   println(i)
    } 
  //  println(gap)
    if(gap==1 && counter!=0)
    0
     else gap
  }
}
