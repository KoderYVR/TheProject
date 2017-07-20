$status = array('OPEN','CLOSE');
$trans=readcontents('connector1');

foreach($trans as $item){
  if($item->status -match $status){
     processTrans($item);
  }
}
