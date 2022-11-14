<?php
$nilai = 80;
echo "Nilai = $nilai";
echo "<hr>";
if($nilai >= 80 and $nilai <= 100 ) { echo "A"; }
if($nilai >= 70 and $nilai < 80 ) { echo "B"; }
if($nilai >= 60 and $nilai < 70 ) { echo "C"; }
if($nilai >= 50 and $nilai < 60 ) { echo "D"; }
if($nilai >= 0 and $nilai < 50 ) { echo "E"; }
?>
<hr>
konversi nilai dengan function
<hr>
<?php

function nilai($int)
{
	if($int >= 80 and  $int  <= 100 ) { $nilai = "A"; }
	if($int >= 70 and  $int  < 80   ) { $nilai = "B"; }
	if($int >= 60 and  $int  < 70   ) { $nilai = "C"; }
	if($int >= 50 and  $int  < 60   ) { $nilai = "D"; }
	if($int >= 0  and  $int  < 50   ) { $nilai = "E"; }
	return $nilai;
}

$nilai = 80;
echo "Nilai = $nilai grade anda adalah ".nilai($nilai);
?>
<hr>
<form action="index.php" method="get">
<input type="text" name="mk" placeholder="Nama Mata kuliah">
 <input type="number" name="nilai" placeholder="Nilai">
 <input type="submit" name="btn" value="konversi">
</form>
<hr>
Hasil..
<hr>
<?php
if(isset($_GET['btn']))
{
	echo "Mata Kuliah : ".$_GET['mk']."<br>";
	echo "Nilai : ".$_GET['nilai']." ( ".nilai($_GET['nilai'])." )";
}
?>