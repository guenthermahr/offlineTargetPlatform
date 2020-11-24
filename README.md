# offlineTargetPlatform
What I do: 
1. I set the online.target to be the active target platform
2. I use the export wizard in feature.xml to crate a folder offlineSite that after execution contains a p2-site.
   Here the problem alsready described occurs: I get entries for the launchers in the artifacts.jar but no 
   org.eclipse.equinox.executable.jar. Currently I have not added the org.eclipse.equinox.executable to the 
   "Included features" of the feature.xml but it doesn't seem to make any difference if I do.
   As Tycho doesn't find the executable feature jar, an error occurs during the build. 
   I cannot upload the whole offlineSite folder - it's to big.
3. In order to solve the problem I created another "executeSite" with only the orge.eclipse.equinox.executable in it - as a source folder as well as a jar. 
   I use the FeaturesAndBundlesPublisher.bat to crate the artifacts.jar and the content.jar
4. If I run it this way using com.initka.nui.target.target for Tycho the build works but there is no eclipse.exe in the resulting product.
5. Please tell me if you need more information.
