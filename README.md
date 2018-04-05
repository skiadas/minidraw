MiniDraw
========

Purpose
---

**MiniDraw** is a teaching-oriented 2D graphics direct manipulation
framework in Java, inspired by JHotDraw.  It is used in the book
*Flexible, Reliable Software - using Patterns and Agile Development*,
by Henrik Bærbak Christensen, published by CRC Press 2010.

Credits
---

The architecture and some of the code base is from JHotDraw 5.1.

Prereqs
---

To compile you need gradle in version 4.6, not standard in a Linux
box. Go to the root of this project and issue

    gradle wrapper
    
And then always use './gradlew', the gradle wrapper, to execute stuff.

Note: You may have to comment out the two includes in `settings.gradle`
to make this work. Reenable the includes again after installing the
gradle wrapper.

How to Use
---

The project contains two folders

  * minidraw/minidraw: the MiniDraw library source code
  * minidraw/demo: demonstration of various MiniDraw features.
  
A simple MiniDraw application is the LogoPuzzle:

    ./gradlew :demo:puzzle
    
which shows a simple puzzle, from Chapter 30 of *Flexible, Reliable
Software*.

Review the `build.gradle` file in folder `demo` for a complete list of
demonstrations.

Note that these demonstration programs will link directly to the
compiled minidraw project, not to the published version on BinTray.


How to publish
---

**Note** It is only the author of MiniDraw who is allowed to publish.

   1. Ensure the BINTRAY_KEY environment variable is set to the
      Bintray key: `export BINTRAY_KEY=thekey`
      
   2. Ensure gradle wrapper is in a new version, `gradle wrapper` in
      the root folder
      
   3. Upload to bintray, `./gradlew :minidraw:bintrayUpload`
   
