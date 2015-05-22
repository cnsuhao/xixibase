# Introduction #
## Xixibase is a high performance, cross platform, distributed cache system. ##
Xixibase server write in C++, based on Boost Asio.

### Xixibase 0.6 ###
Jan-31-2012<br>
<b>Xixibase Server</b>
<ol><li>Add protection on file load<br>
</li><li>Configuration enhancement<br>
</li><li>Support SSL(openSSL)<br>
<b>Xixibase Java Client</b>
</li><li>Support SSL</li></ol>

<h3>Xixibase 0.5</h3>
Dec-7-2011<br>
<b>Xixibase Server</b>
<ol><li>Bug fix<br>
<ul><li>This bug happened after set one big value that size over item_size_max.<br>
</li></ul></li><li>HTTP GZIP support<br>
</li><li>HTTP download from file<br>
</li><li>HTTP Keep-Alive support<br>
</li><li>Introduce Web page tt<br>
</li><li>Update getBase format, do not compatible with old version<br>
</li><li>Other changes<br>
<b>Xixibase Java Client</b>
</li><li>Update getBase format, do not compatible with old version</li></ol>

<h3>Xixibase 0.4</h3>
Nov-14-2011<br>
<b>Xixibase Server</b>
<ol><li>Bug fix<br>
<ul><li>check watch may lead to deadlock<br>
</li></ul></li><li>Log enhancement, the log file is written<br>
<b>Xixibase Java Client</b>
</li><li>Delete the local cache when the client update the server-side data<br>
</li><li>Add some comments<br>
</li><li>Remove some API, such as createDelta<br>
</li><li>Add some examples<br>
</li><li>Javadoc</li></ol>

<h3>Xixibase 0.3</h3>
Nov-5-2011<br>
<b>Xixibase Server</b>
<ol><li>Bug fix<br>
<ul><li>URI decode error for '+'<br>
</li></ul></li><li>Support HTTP 'HEAD' method<br>
</li><li>Support ETag<br>
</li><li>Other little change<br>
<b>Xixibase Java Client</b>
</li><li>Other little change</li></ol>

<h3>Xixibase 0.2</h3>
Nov-2-2011<br>
<b>Xixibase Server</b>
<ol><li>Bug fix<br>
<ul><li>CheckWatch issue<br>
</li><li>delete Peer_Cache async may cause crash<br>
</li><li>update_expiration stats init issue<br>
</li></ul></li><li>Cross platform enhance, like change "%lu" to PRIu32 ...<br>
</li><li>Build enhancement<br>
</li><li>Log enhancement<br>
</li><li>Support HTTP(part)<br>
</li><li>Other little change<br>
<b>Xixibase Java Client</b>
</li><li>Enhance the algorithm of itemSize<br>
</li><li>Default socket noDelay=true<br>
</li><li>Add selector pool for TIME_WAIT issue in windows Multi API</li></ol>

<h3>Xixibase 0.1</h3>
Oct-17-2011<br>
First release, Xixibase Server and Xixibase Java Client<br>
<ol><li>Support 'Local Cache', when client enable 'Local Cache', Client can store the data both Server-side and local, and to ensure local data and Server-side data is consistent. This can greatly increase performance and reduce the pressure on Server and network overhead.<br>
</li><li>Support 'virtualization', 'virtualization' can ensure that different service access the same cache erver, it will not conflict.<br>
</li><li>Support 'MultiAPI', like multiGet, multeUpdate, multiDelete. 'MultiAPI' is a batch processing mode, can provide significant performance.<br>
</li><li>High performance.<br>
</li><li>Cross platform, Xixibase is based on the Boost Asio, in principle, as long as Boost Asio supported platforms, Xixibase can be supported. Like Windows, Linux, Mac.