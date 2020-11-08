---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 53fa3d21089b150a7436311597a88e827f391562
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272181"
---
# <span data-ttu-id="02234-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="02234-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="02234-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02234-102">SYNOPSIS</span></span>
<span data-ttu-id="02234-103">Ändrar ett logiskt program i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="02234-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="02234-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02234-104">SYNTAX</span></span>

### <span data-ttu-id="02234-105">Förbrukning (standard)</span><span class="sxs-lookup"><span data-stu-id="02234-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02234-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="02234-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02234-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02234-107">DESCRIPTION</span></span>
<span data-ttu-id="02234-108">Cmdleten **set-AzLogicApp** ändrar ett logiskt program med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="02234-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="02234-109">Ett logiskt program är en samling åtgärder eller utlösare definierade i logik program definition.</span><span class="sxs-lookup"><span data-stu-id="02234-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="02234-110">Denna cmdlet returnerar ett **arbets flödes** objekt.</span><span class="sxs-lookup"><span data-stu-id="02234-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="02234-111">Du kan ändra en logik-app genom att ange namn, plats, logik program definition, resurs grupp och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="02234-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="02234-112">En logik program definition och parametrar är formaterade i Java Script Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="02234-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="02234-113">Du kan använda ett logik program som mall för definitioner och parametrar.</span><span class="sxs-lookup"><span data-stu-id="02234-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="02234-114">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="02234-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="02234-115">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="02234-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="02234-116">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="02234-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="02234-117">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="02234-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="02234-118">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="02234-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="02234-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02234-119">EXAMPLES</span></span>

### <span data-ttu-id="02234-120">Exempel 1: ändra ett logiskt program</span><span class="sxs-lookup"><span data-stu-id="02234-120">Example 1: Modify a logic app</span></span>
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

<span data-ttu-id="02234-121">Det här kommandot ändrar en logik-app.</span><span class="sxs-lookup"><span data-stu-id="02234-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="02234-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02234-122">PARAMETERS</span></span>

### <span data-ttu-id="02234-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="02234-123">-AppServicePlan</span></span>
<span data-ttu-id="02234-124">Anger namnet på en plan.</span><span class="sxs-lookup"><span data-stu-id="02234-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="02234-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02234-125">-DefaultProfile</span></span>
<span data-ttu-id="02234-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="02234-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02234-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="02234-127">-Definition</span></span>
<span data-ttu-id="02234-128">Anger definitionen för en logik-app som ett objekt eller en sträng i JSON-format (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="02234-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="02234-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="02234-129">-DefinitionFilePath</span></span>
<span data-ttu-id="02234-130">Anger definitionen för en logik-app som sökväg till en definitions fil i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="02234-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="02234-131">-Force</span><span class="sxs-lookup"><span data-stu-id="02234-131">-Force</span></span>
<span data-ttu-id="02234-132">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="02234-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02234-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="02234-133">-IntegrationAccountId</span></span>
<span data-ttu-id="02234-134">Anger ett integrerings konto-ID för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="02234-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="02234-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="02234-135">-Name</span></span>
<span data-ttu-id="02234-136">Anger namnet på en logik-app.</span><span class="sxs-lookup"><span data-stu-id="02234-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="02234-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="02234-137">-ParameterFilePath</span></span>
<span data-ttu-id="02234-138">Anger sökvägen till en JSON-formaterad parameter fil.</span><span class="sxs-lookup"><span data-stu-id="02234-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="02234-139">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="02234-139">-Parameters</span></span>
<span data-ttu-id="02234-140">Anger ett samlings objekt för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="02234-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="02234-141">Ange en hash-tabell, en ord lista \<string\> eller en ord lista \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="02234-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="02234-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02234-142">-ResourceGroupName</span></span>
<span data-ttu-id="02234-143">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="02234-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="02234-144">-State</span><span class="sxs-lookup"><span data-stu-id="02234-144">-State</span></span>
<span data-ttu-id="02234-145">Anger tillståndet för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="02234-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="02234-146">De acceptabla värdena för den här parametern är: Enabled och disabled.</span><span class="sxs-lookup"><span data-stu-id="02234-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="02234-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="02234-147">-UseConsumptionModel</span></span>
<span data-ttu-id="02234-148">Anger att logik programmet använder den förbruknings modellen.</span><span class="sxs-lookup"><span data-stu-id="02234-148">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="02234-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02234-149">-Confirm</span></span>
<span data-ttu-id="02234-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02234-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02234-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02234-151">-WhatIf</span></span>
<span data-ttu-id="02234-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02234-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02234-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02234-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02234-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02234-154">CommonParameters</span></span>
<span data-ttu-id="02234-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02234-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02234-156">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02234-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02234-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02234-157">INPUTS</span></span>

### <span data-ttu-id="02234-158">System. String</span><span class="sxs-lookup"><span data-stu-id="02234-158">System.String</span></span>

## <span data-ttu-id="02234-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02234-159">OUTPUTS</span></span>

### <span data-ttu-id="02234-160">System. Object</span><span class="sxs-lookup"><span data-stu-id="02234-160">System.Object</span></span>

## <span data-ttu-id="02234-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02234-161">NOTES</span></span>

## <span data-ttu-id="02234-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02234-162">RELATED LINKS</span></span>

[<span data-ttu-id="02234-163">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="02234-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="02234-164">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="02234-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="02234-165">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="02234-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="02234-166">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="02234-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


