### How to fix installed build tools revision 31 is corrupted in android studio
https://www.youtube.com/watch?v=lUGRTjTBXYQ

### FragmentManager
move one fragment to another fragment via fragmentmanager

```java
public void onClick(View v) {  
    switch (v.getId())
	{  
        case R.id.createMatchCard:  
            CreateMatch_Fragment createMatch_fragment = new CreateMatch_Fragment();  
 fragmentManager.beginTransaction().replace(R.id.frame_layout,createMatch_fragment).addToBackStack("Home").commit();  
 break; case R.id.uploadCard:  
            Upload_Fragment upload_fragment = new Upload_Fragment();  
 fragmentManager.beginTransaction().replace(R.id.frame_layout,upload_fragment).addToBackStack("Home").commit();  
 break; case R.id.deleteMatchCard:  
            Delete_Fragment delete_fragment = new Delete_Fragment();  
 fragmentManager.beginTransaction().replace(R.id.frame_layout,delete_fragment).addToBackStack("Home").commit();  
 break; 
 }
 ```
 