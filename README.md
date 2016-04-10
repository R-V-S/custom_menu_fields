The Custom Menu Fields module allows administrators to add variables to menus and 
menu items, primarily for purposes of development or theming. Examples of 
useful scenarios for this module:

- Add a subtitle field to your menu items
- Assign parent items to menus or menu items
- Add a taxonomy to your menus and set it as a Workbench Access filter 

## Installation

Place this folder and all subfolders into your modules directory (e.g. 
sites/all/modules/menu_fields)

Enable the Custom Menu Fields module from Drupal's module list (admin/modules in 
Drupal 7).

Set the appropriate permissions. Custom Menu Fields creates two permissions: One for 
administering Custom Menu Fields, and another for ignoring menu restrictions. The 
latter is only relevant if you are using Custom Menu Fields in conjunction with 
Workbench Access. 

## Pages Altered By This Module

admin/structure/menu : If restrictions are used, the list is limited to the 
current user's Workbench Access sections

node/add/page : Menu list is restricted


## How to use Custom Menu Fields

Add, modify or remove fields at: admin/structure/menu_fields

Use the following function to retrieve Menu Field data:

`menu_fields_get_value($item_id, $mfid)` returns the value of a given menu (or menu item) field where `$item_id` is the menu or menu item ID and `$mfid` is either the name of the field or the ID of the field. Using the ID yields better performance. The ID is displayed at admin/structure/menu_fields

