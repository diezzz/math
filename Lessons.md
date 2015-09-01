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

#factoriel
[int]$inputNumber= Read-Host "Моля въведете стойност: ";
$result=0;
$result=($inputNumber)*($inputNumber-1);
for($i=$inputNumber-2; $i -gt 0; $i--){
    $result=$result*$i;
}
Write-Host $result;
