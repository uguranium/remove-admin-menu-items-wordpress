# Remove Admin Menu Items

Put example code your template function file. If template didn't created by yourself. Please put code in the child theme functions.php

Example Code:

```
function remove_menu_items(){
        remove_menu_page( 'themes.php' );
        remove_menu_page( 'plugins.php' );
        remove_submenu_page( 'options-general.php','options-media.php' );
        remove_submenu_page( 'options-general.php','options-general.php' );
}

add_action( 'admin_menu', 'remove_menu_items');
```

*Menu Pages*

```
  remove_menu_page( 'index.php' );                  //Dashboard
	remove_menu_page( 'edit.php' );                   //Posts
	remove_menu_page( 'upload.php' );                 //Media
	remove_menu_page( 'edit.php?post_type=page' );    //Pages
	remove_menu_page( 'edit-comments.php' );          //Comments
	remove_menu_page( 'themes.php' );                 //Appearance
	remove_menu_page( 'plugins.php' );                //Plugins
	remove_menu_page( 'users.php' );                  //Users
	remove_menu_page( 'tools.php' );                  //Tools
	remove_menu_page( 'options-general.php' );        //Settings
```

*Sub Menu Pages*
```
  remove_submenu_page( 'options-general.php','options-media.php' );
  remove_submenu_page( 'options-general.php','options-general.php' );
  remove_submenu_page( 'options-general.php','options-writing.php' );
  remove_submenu_page( 'users.php','users.php' );
  remove_submenu_page( 'users.php','user-new.php' );
  ...
```

*User Limited Pages*

```
if (get_current_user_id() != 1) {
  // Your code here
}
```
