```
/**
* @var $fileType
**/
$formUpload = $this->createFormBuilder()->add('file', FileType::class)->getForm();

$your_big_array = array();
$_file = $formUpload['file']->getData();

/**
* Check if file exist
**/
if (($h = fopen("{$_file}", "r")) !== FALSE) {
   while (($data = fgetcsv($h, 1000, ",")) !== FALSE) {
     // set data equals to your init array
     $your_big_array[] = $data;
  }
  
  /**
  * Shift the first array if not needed
  **/
  array_shift($your_big_array);
  
  // foreach your big array content
  foreach ($your_big_array as $value) {
    // Your own logique to set data
    
    for ($a = 0; $a < count($your_big_array); $a++) {
      // your own logique to insert data
    }
  }
}

```
