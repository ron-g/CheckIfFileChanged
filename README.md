# CheckIfFileChanged
Powershell to check if a file has changed. 

Works in my environment. YMMV.

The files I'm examining should always be growing, so that's why the output is sorted as such. The files also don't change on the weekend, so duplicate MD5 checksums on weekends shouldn't be alarming.

`CheckIfFileChanged.ps1 -LookBackXDays 10 -SrcPath \\AnalyticsServer.ad.example.com\C$\temp -FileName "Finance_Data_*.tab" -SmbUser ad\administrator`


    BaseName              Size (KB) FileHash                         Is Weekend LastWriteTime
    --------              --------- --------                         ---------- -------------
    Finance_Data_06122019 6708      bb2e91a29ecd8294129768fafdce86c8            2019-06-12 22:32:19
    Finance_Data_06132019 6727      480083fb68fa9a6d9acae635b4383106            2019-06-13 22:32:32
    Finance_Data_06142019 6780      123c0c42cd27a4d90480c6b84fb109e0            2019-06-14 22:32:21
    Finance_Data_06152019 6806      0ef019734d2107d3ca2c7a63927099b0 Y          2019-06-15 22:32:20
    Finance_Data_06162019 6806      0ef0197347e107d3ca2c7a63927099b0 Y          2019-06-16 22:32:22
    Finance_Data_06172019 6859      04aec641ee2f4af46872f5e8f330138b            2019-06-17 22:32:29
    Finance_Data_06182019 6912      107708fdfe5d23ac9e16524845e6884b            2019-06-18 22:32:28
    Finance_Data_06192019 6950      1a5f531792795316f38a7c466b515cea            2019-06-19 22:32:37
    Finance_Data_06202019 6978      2a86bfcea28d856144a17a303b57df9b            2019-06-20 22:32:34
    Finance_Data_06212019 7018      8a800d7f155a2788e77988ada8238885            2019-06-21 22:32:26
    
    
    
    
    All Done!
    
    
    Press Enter to continue...:
