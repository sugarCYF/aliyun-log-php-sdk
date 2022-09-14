# Aliyun Log Service PHP SDK

## Modify

~~~ shell
diff --git a/Aliyun/Log/Client.php b/Aliyun/Log/Client.php
--- a/Aliyun/Log/Client.php
+++ b/Aliyun/Log/Client.php
@@ -242,7 +242,7 @@ class Aliyun_Log_Client {
         $logGroup->setSource ( $source );
         $logitems = $request->getLogitems ();
         foreach ( $logitems as $logItem ) {
-            $log = new Log ();
+            $log = new SlsLog ();^M
             $log->setTime ( $logItem->getTime () );
             $content = $logItem->getContents ();
             foreach ( $content as $key => $value ) {
             
             
diff --git a/Aliyun/Log/sls.proto.php b/Aliyun/Log/sls.proto.php
--- a/Aliyun/Log/sls.proto.php
+++ b/Aliyun/Log/sls.proto.php
@@ -126,7 +126,7 @@ class Log_Content {
 }
 
 // message Log
-class Log {
+class SlsLog {
   private $_unknown;
 
   function __construct($in = NULL, &$limit = PHP_INT_MAX) {

~~~