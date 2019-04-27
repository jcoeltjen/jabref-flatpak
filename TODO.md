# TODO
- [ ] find a solution for missing `cacerts` in imported jdk that does not rely on locally installed Java
- [ ] make JabRef version configurable
- [ ] reduce size of end artifact
- [ ] add scripts to build to single file 
- [ ] include webkit

## Errors

### Webkit missing and fallback renderer is used
```
16:22:46.978 [JavaFX Application Thread] ERROR org.jabref.FallbackExceptionHandler - Uncaught exception occurred in Thread[JavaFX Application Thread,5,main]
java.lang.UnsatisfiedLinkError: Can't load library: /app/jdk/jre/lib/amd64/libjfxwebkit.so
	at java.lang.ClassLoader.loadLibrary(ClassLoader.java:1827) ~[?:1.8.0-internal]
	at java.lang.Runtime.load0(Runtime.java:809) ~[?:1.8.0-internal]
	at java.lang.System.load(System.java:1086) ~[?:1.8.0-internal]
	at com.sun.glass.utils.NativeLibLoader.loadLibraryFullPath(NativeLibLoader.java:201) ~[jfxrt.jar:?]
	at com.sun.glass.utils.NativeLibLoader.loadLibraryInternal(NativeLibLoader.java:94) ~[jfxrt.jar:?]
	at com.sun.glass.utils.NativeLibLoader.loadLibrary(NativeLibLoader.java:39) ~[jfxrt.jar:?]
	at com.sun.webkit.WebPage.lambda$static$0(WebPage.java:133) ~[jfxrt.jar:?]
	at java.security.AccessController.doPrivileged(Native Method) ~[?:1.8.0-internal]
	at com.sun.webkit.WebPage.<clinit>(WebPage.java:132) ~[jfxrt.jar:?]
	at javafx.scene.web.WebEngine.<init>(WebEngine.java:881) ~[jfxrt.jar:?]
	at javafx.scene.web.WebEngine.<init>(WebEngine.java:868) ~[jfxrt.jar:?]
	at javafx.scene.web.WebView.<init>(WebView.java:273) ~[jfxrt.jar:?]
	at org.jabref.gui.PreviewPanel.lambda$new$1(PreviewPanel.java:82) ~[JabRef-4.3.1.jar:?]
	at com.sun.javafx.application.PlatformImpl.lambda$null$5(PlatformImpl.java:295) ~[jfxrt.jar:?]
	at java.security.AccessController.doPrivileged(Native Method) ~[?:1.8.0-internal]
	at com.sun.javafx.application.PlatformImpl.lambda$runLater$6(PlatformImpl.java:294) ~[jfxrt.jar:?]
	at com.sun.glass.ui.InvokeLaterDispatcher$Future.run(InvokeLaterDispatcher.java:95) ~[jfxrt.jar:?]
	at com.sun.glass.ui.gtk.GtkApplication._runLoop(Native Method) ~[jfxrt.jar:?]
	at com.sun.glass.ui.gtk.GtkApplication.lambda$null$10(GtkApplication.java:245) ~[jfxrt.jar:?]
	at java.lang.Thread.run(Thread.java:748) [?:1.8.0-internal]
16:22:47.355 [JavaFX Application Thread] ERROR org.jabref.FallbackExceptionHandler - Uncaught exception occurred in Thread[JavaFX Application Thread,5,main]
java.lang.NullPointerException: null
	at org.jabref.gui.PreviewPanel.lambda$setPreviewLabel$15(PreviewPanel.java:259) ~[JabRef-4.3.1.jar:?]
	at com.sun.javafx.application.PlatformImpl.lambda$null$5(PlatformImpl.java:295) ~[jfxrt.jar:?]
	at java.security.AccessController.doPrivileged(Native Method) ~[?:1.8.0-internal]
	at com.sun.javafx.application.PlatformImpl.lambda$runLater$6(PlatformImpl.java:294) ~[jfxrt.jar:?]
	at com.sun.glass.ui.InvokeLaterDispatcher$Future.run(InvokeLaterDispatcher.java:95) ~[jfxrt.jar:?]
	at com.sun.glass.ui.gtk.GtkApplication._runLoop(Native Method) ~[jfxrt.jar:?]
	at com.sun.glass.ui.gtk.GtkApplication.lambda$null$10(GtkApplication.java:245) ~[jfxrt.jar:?]
	at java.lang.Thread.run(Thread.java:748) [?:1.8.0-internal]
```
