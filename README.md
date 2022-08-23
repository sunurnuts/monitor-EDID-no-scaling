# monitor-EDID-no-scaling
monitor registry files for 1920x1080 no scaling (scaling=2)

instructions: 

1.reset-all.exe

2.restart64.exe
<details>(you have to do this before running registry file otherwise it does weird stuff im not sure about you can try doing it after to see how it feels) (reason being reset-all.exe delets graphicsdriver contents and EDID content, and other places in registry fetch data from there, if you dont restart64 and instead try to update edid i am not sure what happens i need to learn more)
  </details>
  
3.run your registry file with exported CRU EDID override (i have my example registry uploaded)
4.restart64.exe (check DefaultSettings.DriverExtra located in the HKLM\SYSTEM\CurrentControlSet\Hardware Profiles\UnitedVideo\CONTROL\VIDEO\ to make sure it has the scaling set to 02)


what the registry file does:

1.deletes the default EDID

2.adds the CRU EDID changes shown in the image to the registry

3.changes scaling=2 (no scaling)

4.deletes the unitedvideo (so it can refetch the data like scaling when u restart64 on cru or turn off then on monitor)
