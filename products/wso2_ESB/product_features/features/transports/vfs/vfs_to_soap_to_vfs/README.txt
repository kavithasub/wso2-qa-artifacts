This scenario will test VFS will read a file contains a soap message and pass it on to the backend (endpoint) where simple stock quote service deployed. Then saved the response message to a file system using the file name by concatnate the MessageID and uuid. Here the action after processing is move. The successful processing result in original file will be move to Pass folder and any failure result in file being move to Failures folder.

1. Enable VFS transport and create a stockQuoteProxy (Synapse vfsFileStockQuoteProxy.xml)

2. Create a folder stucture like below
C:\PERSONAL\VFS
├───Failures
├───Original
├───out
└───Pass

3. Deploy SimpleStockQuote Service using AXIS2

4. Place the Test.XML & aaa.xml to Original folder

5. Results
Test.XML should move to Pass folder
aaa.xml should move to Failures folder
AXIS2 response should saved to out folder (Using Test.xml)


VFS - Sample 254 for basic functionality