Release History of MiniDraw
===========================

 * Pre 1.0: Many many releases for various course instances.

 * 1.0: Version of MiniDraw at the time of book submission to CRC Press.

 * 1.1: Defect in boardgame hotspots fixed. Move from a location to
   the same location would not readjust the figure on the graphical
   location.

 * 1.2: Reduced the number of hotspots associated with the positioning
   strategy in the boardgame extensions.
  
 * 1.3: Changes introduced to handle 'props' in the BoardGame
   extension of MiniDraw.

 * 1.4: Some defensive programming techniques introduced in BoardGame
   extension.
 
 * 1.5: Fixed bug concerning movement of props in BoardGame. Minor documentation
   changes.
  
 * 1.6: Fixed bug in BoardGame's BoardActionTool concerning actions
   performed on props that return false.
  
 * 1.7: Several changes made in the notification and repainting
   sequence as some defects were discovered (which actually are
   embedded in the original JHotDraw code as well.) See comment in the
   source code below.
  
 * 1.8: Added hook method in MiniDrawApplication to override windows close
   operation.
  
 * 1.9: Updated ImageManager so a) it also looks for image files in a
   folder /resources to make it work together with gradle more easily,
   b) also will load PNG and JPG files (having '.png' or '.jpg'
   suffixes).
 
 * 1.10: Updated ImageManager so a) actually works in a gradle
   context: put all your wanted images in
   /src/main/resources/minidraw/ subfolder in the default gradle
   project structure.
 
 * 1.11: Redefined the image folder for Gradle builds to be
  /src/main/resources/minidraw-images to avoid conflicts in resource
  loading
  
 * 1.12: Moved MiniDraws to open source on BitBucket, created
   deployment structure using gradle, uploaded to JCenter.
