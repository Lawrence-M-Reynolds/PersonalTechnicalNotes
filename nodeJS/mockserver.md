https://www.npmjs.com/package/mockserver

__Create folder__
C:\Development\npmProjects\mockserver
/mnt/c/Development/npmProjects/mockserver

C:\Development\npmProjects\mockserver\mocks\aggregator\updatemarketingref
Add file "POST.mock" in this directory with the following contents:

```
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8

<UpdateMarketingReferenceResult>
    <updateMarketingRefResponse>
        <StatusOK>true</StatusOK>
        <StatusMessage>999/6667/B156/WEB updated from quotezone to quotezone</StatusMessage>
    </updateMarketingRefResponse>
</UpdateMarketingReferenceResult>
```

__Initialise__
cd C:\Development\npmProjects\mockserver
npm init

npm install -g mockserver
mockserver -p 8080 -m mocks

__Day to day__
cd C:\Development\npmProjects\mockserver
mockserver -p 8080 -m mocks