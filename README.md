# PluginMCreator

Test divers méthode, bientôt du freemaker


	<#list data.getComponentsOfType("TextField") as component>
	EditBox ${component.getName()};
	</#list>



<#macro buttonOnClick buttonName>
    e -> {
        if (<@procedureOBJToConditionCode component.displayCondition/>) {
            PacketDistributor.SERVER.noArg().send(new ${name}ButtonMessage(${btid}, x, y, z, ${buttonName}.getValue()));
            ${name}ButtonMessage.handleButtonAction(entity, ${btid}, x, y, z, ${buttonName}.getValue());
        }
    }
</#macro>
