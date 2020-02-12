# codesignal-practice-test in PHP
The answers fro the codeSignal Practice Exam. The questions will be added if i can get them

### TinyPairs

```
function tinyPairs($a,$b,$k){
    $pairs = 0;
    foreach($a as $i => $x){
        $y = sizeOf($b) - $i;
        $sum_str =(int) $x.$y; 
        $sum = (int) $sum_str;        
        // echo "( $x, $y ) =  ";
        // var_dump($sum);        
        if($sum < $k ){
           // echo "true \n -------------- \n";
            $pairs++;
        }
    }    
    return $pairs;
}

// example data
$a = [1,2,3];
$b = [1,2,3];
$k = 31;
 ```
    
### MeanGroups
```
function meanGroups($a){
    $d=[]; //indexes
    $e=[]; //results    
    foreach($a as $i=>$j){
        $avg = array_sum($j)/count($j);
        echo "avg for index $i is $avg \n";
        if (! in_array($avg, $e)) { //if the average not exists
            // put it into the results
            array_push ($e,$avg);
            //put it inside the indexes
            array_push($d,[$i]);
        }else{ //the average exists in the array
            array_push($d[array_search($avg,$e)], $i);
        }
    }
    var_dump($e);
    return $d;
}

//example data
$a = [
  [4,4,0,4],
  [2,2],
  [3,3,3],
  [4,4,4,4]
];

```
