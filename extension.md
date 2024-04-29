we can add extension through UI or we can add plugin manually

  First I can show how we can add plugin manually for reference kindly check plugin.xml

     Plugin Description:

<extension point="org.eclipse.ui.commands">: This line declares an extension point for commands in the Eclipse IDE. It allows you to define new commands and their associated behavior.

<category id="com.lmkr.hello.category" name="HelloWorld Category">: This defines a category for organizing commands. In this case, it’s named “HelloWorld Category” with the unique identifier “com.lmkr.hello.category.”

<command categoryId="com.lmkr.hello.category" name="HelloWorld Command" id="com.lmkr.hello.helloCommand">: Here, a new command is declared. It belongs to the previously defined category (“HelloWorld Category”) and has the name “HelloWorld Command.” Its unique identifier is “com.lmkr.hello.helloCommand.”

<handler class="com.lmkr.hello.HelloHandler" commandId="com.lmkr.hello.helloCommand">: This line associates a handler class (com.lmkr.hello.HelloHandler) with the “HelloWorld Command.” The handler defines the actual behavior when the command is executed.

<key commandId="com.lmkr.hello.helloCommand" schemeId="org.eclipse.ui.defaultAcceleratorConfiguration" contextId="org.eclipse.ui.contexts.window" sequence="M1+6">: This specifies a key binding for the command. When the user presses the specified key combination (in this case, “M1+6”), the associated command will be triggered.

<menuContribution locationURI="menu:org.eclipse.ui.main.menu?after=additions">: This contributes a new menu item to the main menu of the Eclipse IDE. It appears after existing menu items.

<menu id="com.lmkr.hello.helloMenu" label="Hello Menu" mnemonic="M">: Defines a menu item named “Hello Menu” with the mnemoni “M.”

<command commandId="com.lmkr.hello.helloCommand" id="HelloWorld.menus.sampleCommand" mnemonic="S">: Associates the “HelloWorld Command” with the menu item. When the user selects this menu item, the associated command will be executed.

<menuContribution locationURI="toolbar:org.eclipse.ui.main.toolbar?after=additions">: Similar to the menu contribution, this adds a toolbar item to the main toolbar of the Eclipse IDE.

<toolbar id="com.lmkr.hello.helloToolbar">: Declares a toolbar item with the ID “com.lmkr.hello.helloToolbar.”

<command id="HelloWorld.toolbars.sampleCommand" commandId="com.lmkr.hello.helloCommand" icon="icons/sample.png" tooltip="Say hello world">: Associates the “HelloWorld Command” with the toolbar item. It also specifies an icon (“icons/sample.png”) and a tooltip (“Say hello world”).


In summary, this XML snippet defines a new command (“HelloWorld Command”) with associated categories, handlers, key bindings, menu items, and toolbar items in the Eclipse IDE. The command’s behavior is implemented by the specified handler class.