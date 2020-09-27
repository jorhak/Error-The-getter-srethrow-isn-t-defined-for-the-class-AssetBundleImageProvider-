# Error: The getter 'srethrow' isn't defined for the class 'AssetBundleImageProvider' ⚠️⚠️⚠️

```
Running "flutter pub get" in componentes...                         0,5s
Your Flutter application is created using an older version of the Android
embedding. It's being deprecated in favor of Android embedding v2. Follow the
steps on https://flutter.dev/go/android-project-migration to migrate your
project.
Launching lib/main.dart on SM J610G in debug mode...
[!] Your app isn't using AndroidX.
    To avoid potential build failures, you can quickly migrate your app by
    following the steps on https://goo.gl/CP92wY .
../../Android/flutter/packages/flutter/lib/src/painting/image_provider.dart:672:7: Error: The getter 'srethrow' isn't defined for the class 'AssetBundleImageProvider'.
 - 'AssetBundleImageProvider' is from 'package:flutter/src/painting/image_provider.dart' ('../../Android/flutter/packages/flutter/lib/src/painting/image_provider.dart').
Try correcting the name to the name of an existing getter, or defining a getter or field named 'srethrow'.
      srethrow;                                                         
      ^^^^^^^^                                                          
                                                                        
                                                                        
_FAILURE: Build failed with an exception.                                
                                                                        
* Where:                                                                
Script '/home/jon/Android/flutter/packages/flutter_tools/gradle/flutter.gradle' line: 896
                                                                        
* What went wrong:                                                      
Execution failed for task ':app:compileFlutterBuildDebug'.              
> Process 'command '/home/jon/Android/flutter/bin/flutter'' finished with non-zero exit value 1
                                                                        
* Try:                                                                  
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output. Run with --scan to get full insights.
                                                                        
* Get more help at https://help.gradle.org                              
                                                                        
BUILD FAILED in 10s                                                     
Running Gradle task 'assembleDebug'...                                  
Running Gradle task 'assembleDebug'... Done                        11,3s
Exception: Gradle task assembleDebug failed with exit code 1
```

_me salio este error y lo solucione haciendo lo siguiente_
* me dirigi al archivo que estaba en mi caso en la direccion ../Android/flutter/packages/flutter/lib/src/painting/image_provider.dart como me salia
en el error
*una vez ahi me dirigi a la linea 672 en esa linea estaba escrito lo siguiente:
   srethrow;
*lo que hice fue reemplazarla con: rethrow;
*hecho esto se soluciono el problema.

## Ahora cuando lo ejecuto me sale lo siguiente: ✔️✔️✔️
```
Your Flutter application is created using an older version of the Android
embedding. It's being deprecated in favor of Android embedding v2. Follow the
steps on https://flutter.dev/go/android-project-migration to migrate your
project.
Launching lib/main.dart on SM J610G in debug mode...
[!] Your app isn't using AndroidX.
    To avoid potential build failures, you can quickly migrate your app by
    following the steps on https://goo.gl/CP92wY .
Running Gradle task 'assembleDebug'...                                  
Running Gradle task 'assembleDebug'... Done                        42,5s
✓ Built build/app/outputs/flutter-apk/app-debug.apk.
Installing build/app/outputs/flutter-apk/app.apk...                19,3s
Waiting for SM J610G to report its views...                         74ms
Syncing files to device SM J610G...                                998ms

Flutter run key commands.
r Hot reload. 🔥🔥🔥
R Hot restart.
h Repeat this help message.
d Detach (terminate "flutter run" but leave application running).
c Clear the screen
q Quit (terminate the application on the device).
An Observatory debugger and profiler on SM J610G is available at:
http://127.0.0.1:46171/TwLAWiE9SLw=/
```
_y eso es todo_
