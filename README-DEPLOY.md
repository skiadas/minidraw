MiniDraw Deployment Information
========

Purpose
---

Internal documentation of how to deploy MiniDraw to BinTray.

Prereqs
---

To upload you need gradle in version 4.6, which is not standard in a
Linux box. Go to the root of this project and issue

    gradle wrapper
    
And then always use './gradlew', the gradle wrapper, to execute stuff.

Note: You may have to comment out the two includes in `settings.gradle`
to make this work. Reenable the includes again after installing the
gradle wrapper.


How to publish
---

**Note** It is only the author of MiniDraw who is allowed to publish.

   1. Ensure the BINTRAY_KEY environment variable is set to the
      Bintray key: `export BINTRAY_KEY=thekey`.
      
   2. Ensure gradle wrapper is in a newer version, `gradle wrapper` in
      the root folder.
   
   3. Update the `props.minidrawversion` property in
      `minidraw/build-deploy.gradle` to the new version of MiniDraw;
      and update
      the [version description](minidraw/version-history.md).
   
   4. Update the VERSION constant in source file DrawingEditor in
      MiniDraw.
      
   5. Verify by `./gradlew -b minidraw/build-deploy.gradle
      publishToMaveLocal` which publishes to the local .m2 folder,
      that POM files and other artefacts are correct.
      
   6. Upload to bintray, `./gradlew clean :minidraw:bintrayUpload`.
   
   7. In the bintray web page, first publish the artefacts, next
      choose upload to JCenter.
   
