# Exile-Change-Construction-Pin

This enables PIN code change on objects like doors/gates/hatches/drawbridges etc. So you don't have to remove and replace an object to change the PIN code.


# Installation 
* Replace @ExileServer\addons\exile_server\code\ExileServer_object_lock_network_setPin.sqf

* Add this to class Construction of the CfgInteractionMenus inside mission config.cpp

        class ChangePinCode : ExileAbstractAction
        {
        		title = "Change PIN";
        		condition = "((ExileClientInteractionObject getvariable ['ExileIsLocked',1]) isEqualTo 0) && (call ExileClient_util_world_isInOwnTerritory)";
        		action = "_this spawn ExileClient_object_lock_setPin";
        };

# License Info: If you server is named KFB (Kentucky Fried Bambi) you have no permission to use this. Any violation will result in a DMCA.
