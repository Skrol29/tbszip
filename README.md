# TbsZip

  
[TbsZip ][1] is a simple PHP class that helps to work with zip archives. 
You can **read**, **modify**, or **create** a zip archive.
No exe file is needed, and no temporary files are created.

Documentation
-------------------

[Help file][2]

Examples
------------
```
// Reading contents
$zip = new clsTbsZip();
$zip->Open('archive1.zip');
if ($zip->FileExists('subfile2.txt')) {
	$data = $zip->FileRead('subfile2.txt');
}
$zip->Close();
```

```
// Writing contents
$zip = new clsTbsZip();
$zip->Open('archive1.zip');
$zip->FileReplace('subfile2.txt', $txt, TBSZIP_STRING);
$zip->Flush(TBSZIP_FILE, 'archive1_new.zip'); // save the modifications as a new archive
$zip->Close();
```

```
// Creating a new archive
$zip = new clsTbsZip();
$zip->CreateNew();
$zip->FileAdd('newfile.txt', $data, TBSZIP_STRING);
$zip->Flush(TBSZIP_FILE, 'archive1_new.zip'); // save the modifications as a new archive
$zip->Close();
```

```
// Direct download without saving
$zip->Flush(TBSZIP_DOWNLOAD, 'download.zip'); // see doc fore more options
```


[1]: https://www.tinybutstrong.com/tbszip.php
[2]:https://www.tinybutstrong.com/tbszip.php#synopsis

