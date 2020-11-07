---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 254ab4f1dd126e1b671c9a1d899a9dbe8e71beca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743725"
---
# <span data-ttu-id="69608-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69608-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="69608-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69608-102">SYNOPSIS</span></span>
<span data-ttu-id="69608-103">Ändrar ett logiskt program i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="69608-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="69608-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69608-104">SYNTAX</span></span>

### <span data-ttu-id="69608-105">Förbrukning (standard)</span><span class="sxs-lookup"><span data-stu-id="69608-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69608-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="69608-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69608-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69608-107">DESCRIPTION</span></span>
<span data-ttu-id="69608-108">Cmdleten **set-AzLogicApp** ändrar ett logiskt program med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="69608-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="69608-109">Ett logiskt program är en samling åtgärder eller utlösare definierade i logik program definition.</span><span class="sxs-lookup"><span data-stu-id="69608-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="69608-110">Denna cmdlet returnerar ett **arbets flödes** objekt.</span><span class="sxs-lookup"><span data-stu-id="69608-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="69608-111">Du kan ändra en logik-app genom att ange namn, plats, logik program definition, resurs grupp och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="69608-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="69608-112">En logik program definition och parametrar är formaterade i Java Script Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="69608-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="69608-113">Du kan använda ett logik program som mall för definitioner och parametrar.</span><span class="sxs-lookup"><span data-stu-id="69608-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="69608-114">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="69608-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="69608-115">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="69608-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="69608-116">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="69608-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="69608-117">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="69608-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="69608-118">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="69608-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="69608-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69608-119">EXAMPLES</span></span>

### <span data-ttu-id="69608-120">Exempel 1: ändra ett logiskt program</span><span class="sxs-lookup"><span data-stu-id="69608-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="69608-121">Det här kommandot ändrar en logik-app.</span><span class="sxs-lookup"><span data-stu-id="69608-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="69608-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69608-122">PARAMETERS</span></span>

### <span data-ttu-id="69608-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69608-123">-AppServicePlan</span></span>
<span data-ttu-id="69608-124">Anger namnet på en plan.</span><span class="sxs-lookup"><span data-stu-id="69608-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69608-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69608-125">-DefaultProfile</span></span>
<span data-ttu-id="69608-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="69608-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="69608-127">-Definition</span></span>
<span data-ttu-id="69608-128">Anger definitionen för en logik-app som ett objekt eller en sträng i JSON-format (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="69608-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="69608-129">-DefinitionFilePath</span></span>
<span data-ttu-id="69608-130">Anger definitionen för en logik-app som sökväg till en definitions fil i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="69608-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-131">-Force</span><span class="sxs-lookup"><span data-stu-id="69608-131">-Force</span></span>
<span data-ttu-id="69608-132">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="69608-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="69608-133">-IntegrationAccountId</span></span>
<span data-ttu-id="69608-134">Anger ett integrerings konto-ID för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="69608-134">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="69608-135">-Name</span></span>
<span data-ttu-id="69608-136">Anger namnet på en logik-app.</span><span class="sxs-lookup"><span data-stu-id="69608-136">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="69608-137">-ParameterFilePath</span></span>
<span data-ttu-id="69608-138">Anger sökvägen till en JSON-formaterad parameter fil.</span><span class="sxs-lookup"><span data-stu-id="69608-138">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-139">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="69608-139">-Parameters</span></span>
<span data-ttu-id="69608-140">Anger ett samlings objekt för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="69608-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="69608-141">Ange en hash-tabell, en ord lista \< \> eller en ord lista \< , WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="69608-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69608-142">-ResourceGroupName</span></span>
<span data-ttu-id="69608-143">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="69608-143">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69608-144">-State</span><span class="sxs-lookup"><span data-stu-id="69608-144">-State</span></span>
<span data-ttu-id="69608-145">Anger tillståndet för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="69608-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="69608-146">De acceptabla värdena för den här parametern är: Enabled och disabled.</span><span class="sxs-lookup"><span data-stu-id="69608-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="69608-147">-UseConsumptionModel</span></span>
<span data-ttu-id="69608-148">Anger att logik programmet använder den förbruknings modellen.</span><span class="sxs-lookup"><span data-stu-id="69608-148">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69608-149">-Confirm</span></span>
<span data-ttu-id="69608-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69608-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69608-151">-WhatIf</span></span>
<span data-ttu-id="69608-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69608-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69608-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69608-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69608-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69608-154">CommonParameters</span></span>
<span data-ttu-id="69608-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69608-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69608-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69608-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69608-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69608-157">INPUTS</span></span>

### <span data-ttu-id="69608-158">System. String</span><span class="sxs-lookup"><span data-stu-id="69608-158">System.String</span></span>

## <span data-ttu-id="69608-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69608-159">OUTPUTS</span></span>

### <span data-ttu-id="69608-160">System. Object</span><span class="sxs-lookup"><span data-stu-id="69608-160">System.Object</span></span>

## <span data-ttu-id="69608-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69608-161">NOTES</span></span>

## <span data-ttu-id="69608-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69608-162">RELATED LINKS</span></span>

[<span data-ttu-id="69608-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69608-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="69608-164">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69608-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="69608-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69608-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="69608-166">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="69608-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


