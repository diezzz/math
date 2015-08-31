# find prime number with their position
$position=1;
$divider=0;
for($i=2; $position -le 251; $i++){
   $divider=0;
   for($j=1; $j -le $i; $j++){
        if(($i%$j) -eq 0){
            $divider++;
        }
   }
   if($divider -eq 2){
    Write-Host $position"`t"$i;
    $position++;
   }
}
