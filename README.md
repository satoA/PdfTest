PdfTest
=======

PdfTest FileOpenerTest

IBMの公開してくれている、FileOpener.jsを利用してみました。
最高です。


最新版は以下でゲットしてください。
https://github.com/markeeftb/FileOpener

ApacheCordova2.0で大枠を作成後、
xmlフォルダ配下のconfig.xmlに以下を追加。<plugins>のところ。
<plugins>
        <plugin name="FileOpener" value="com.phonegap.plugins.fileopener.FileOpener"/>
</plugins>


src配下にcom.phonegap.plugins.fileopenerパッケージを作り、FileOpener.javaを配置。

index.htmlに以下を追加。
<script type="text/javascript">
function viewFdf(){
	window.plugins.fileOpener.open("file:///sdcard/pdf/requestProcess.pdf");
}
</script>

<body>部分には以下としてボタンを押したらPDFを読むようにした。
<input type="button" value="pdf" onClick="viewFdf()">
