This project has been move to github:
https://github.com/yeaya/xixibase

## Xixibase is a high performance, cross platform, distributed cache system. ##

Xixibase server write in C++, based on Boost Asio.

## Xixibase main highlights: ##
  1. **'Local Cache'**, when client enable 'Local Cache', Client can store the data both Server-side and local, and to ensure local data and Server-side data is consistent. This can greatly increase performance and reduce the pressure on Server and network overhead.
  1. **'virtualization'**, 'virtualization' can ensure that different service access the same cache erver, it will not conflict.
  1. **'MultiAPI'**, like multiGet, multeUpdate, multiDelete. 'MultiAPI' is a batch processing mode, can provide significant performance.
  1. **High performance**.
  1. **Cross platform**, Xixibase is based on the Boost Asio, in principle, as long as Boost Asio supported platforms, Xixibase can be supported. Like Windows, Linux, Mac.
  1. **Support HTTP protocol**, you can directly access the Xixibase Server with browser or JavaScript. Coupled Xixibase the Local Cache feature will greatly reduce the Server's pressure and improve the user experience.
  1. **Support SSL**

## ReleaseNotes ##
http://code.google.com/p/xixibase/wiki/ReleaseNotes<br>
It is strongly recommended to upgrade to version 0.6.<br>
<br>
<h2>Performance Benchmark</h2>
<a href='http://xixibase.googlecode.com/svn/tags/xixibase-0.2/benchmark/java/benchmark2.html'>http://xixibase.googlecode.com/svn/tags/xixibase-0.2/benchmark/java/benchmark2.html</a>
<br><br>

<h2>Performance Comparison</h2>
<a href='http://xixibase.googlecode.com/svn/tags/xixibase-0.2/benchmark/java/benchmark.html'>http://xixibase.googlecode.com/svn/tags/xixibase-0.2/benchmark/java/benchmark.html</a>
<br><br>

<h2>Quick Start:</h2>
Download:<br>
<a href='http://code.google.com/p/xixibase/downloads/list'>http://code.google.com/p/xixibase/downloads/list</a>
<br>
<b>Server:</b><br>
For Linux or Mac:<br>
<pre><code>// build, please refer http://code.google.com/p/xixibase/wiki/BuildXixibaseServer<br>
cd xixibase/bin<br>
./xixibase<br>
</code></pre>
For Windows:<br>
Download xixibase-0.5-win32-bin.zip<br>
<pre><code>// unzip xixibase-0.5-win32-bin.zip<br>
cd xixibase\bin<br>
xixibase.exe<br>
</code></pre>

<b>Browser:</b><br>
Xixibase support HTTP(partially). We can access Xixibase server with browser.<br>
<pre><code>// manager tool<br>
http://localhost:7788/tt/index.html<br>
<br>
// set<br>
http://localhost:7788/manager/set?k=/index.html&amp;v=&lt;h1&gt;hello world!&lt;/h1&gt;<br>
<br>
// get<br>
http://localhost:7788/manager/get?k=/index.html<br>
// or<br>
http://localhost:7788/index.html<br>
</code></pre>

<b>Java Client:</b><br>
Download Xixibase-Client_0.5.jar <br>
Add Xixibase-Client_0.5.jar in your project.<br>

<pre><code>String servers = "localhost:7788,localhost:8877";<br>
String[] serverlist = servers.split(",");<br>
<br>
CacheClientManager mgr = CacheClientManager.getInstance();<br>
mgr.initialize(serverlist);<br>
<br>
CacheClient cc = mgr.createClient("service1");<br>
<br>
// set<br>
cc.set("key", "value");<br>
<br>
// get<br>
String value = (String)cc.get("key");<br>
</code></pre>