---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 4222b50ed941df6f84421cff867845b31744d9e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089122"
---
# <span data-ttu-id="9ef1f-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ef1f-101">New-AzLogicApp</span></span>

## <span data-ttu-id="9ef1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ef1f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef1f-103">Skapar ett logiskt program i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="9ef1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ef1f-104">SYNTAX</span></span>

### <span data-ttu-id="9ef1f-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ef1f-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef1f-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ef1f-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ef1f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ef1f-107">DESCRIPTION</span></span>
<span data-ttu-id="9ef1f-108">Cmdleten **New-AzLogicApp** skapar ett logiskt program med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="9ef1f-109">Ett logiskt program är en samling åtgärder eller utlösare definierade i logik program definition.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="9ef1f-110">Denna cmdlet returnerar ett **arbets flödes** objekt.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="9ef1f-111">Du kan skapa en logik-app genom att ange namn, plats, logik program definition, resurs grupp och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="9ef1f-112">En logik program definition och parametrar är formaterade i Java Script Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="9ef1f-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="9ef1f-113">Du kan använda ett logik program som mall för definitioner och parametrar.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="9ef1f-114">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9ef1f-115">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9ef1f-116">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9ef1f-117">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="9ef1f-118">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="9ef1f-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ef1f-119">EXAMPLES</span></span>

### <span data-ttu-id="9ef1f-120">Exempel 1: skapa ett logiskt program med hjälp av definitions-och parameter fil Sök vägar</span><span class="sxs-lookup"><span data-stu-id="9ef1f-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="9ef1f-121">Det här kommandot skapar ett logiskt program i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="9ef1f-122">Programmet logik innehåller definitionen och parametrarna som anges i fil Sök vägar.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="9ef1f-123">Exempel 2: skapa ett logiskt program med hjälp av definitions-och parameter objekt</span><span class="sxs-lookup"><span data-stu-id="9ef1f-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="9ef1f-124">Det här kommandot skapar ett logiskt program i den angivna resurs gruppen resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="9ef1f-125">Exempel 3: skapa ett logiskt program med hjälp av pipeline för att ange resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9ef1f-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="9ef1f-126">Det här kommandot får resurs gruppen "ResourceGroup11" genom att använda Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="9ef1f-127">Kommandot överför den resurs gruppen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9ef1f-128">Den aktuella cmdleten skapar ett logiskt program i den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="9ef1f-129">Programmet logik innehåller definitionen och parametrarna som anges i fil Sök vägar.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="9ef1f-130">Exempel 4: skapa ett logiskt program baserat på ett befintligt logiskt program</span><span class="sxs-lookup"><span data-stu-id="9ef1f-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="9ef1f-131">Det första kommandot får till gång till logik programmet med namnet LogicApp03 med hjälp av Get-AzLogicApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="9ef1f-132">Kommandot lagrar programmet logik i $Workflow variabel.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="9ef1f-133">Det andra kommandot skapar ett nytt logiskt program som använder definitionen och parametrarna för logik programmet som lagras i $Workflow.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="9ef1f-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ef1f-134">PARAMETERS</span></span>

### <span data-ttu-id="9ef1f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef1f-135">-DefaultProfile</span></span>
<span data-ttu-id="9ef1f-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9ef1f-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ef1f-137">-Definition</span><span class="sxs-lookup"><span data-stu-id="9ef1f-137">-Definition</span></span>
<span data-ttu-id="9ef1f-138">Anger definitionen för din logik-app som ett objekt eller en sträng i JSON-format (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="9ef1f-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef1f-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="9ef1f-139">-DefinitionFilePath</span></span>
<span data-ttu-id="9ef1f-140">Anger definitionen för en logik-app som sökväg till en definitions fil i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef1f-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="9ef1f-141">-IntegrationAccountId</span></span>
<span data-ttu-id="9ef1f-142">Anger ett integrerings konto-ID för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="9ef1f-143">-Plats</span><span class="sxs-lookup"><span data-stu-id="9ef1f-143">-Location</span></span>
<span data-ttu-id="9ef1f-144">Anger platsen för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="9ef1f-145">Ange en plats för Azure Data Center, till exempel West US eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="9ef1f-146">Du kan placera ett logiskt program på valfri plats.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="9ef1f-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ef1f-147">-Name</span></span>
<span data-ttu-id="9ef1f-148">Anger namnet på logik programmet.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-148">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="9ef1f-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="9ef1f-149">-ParameterFilePath</span></span>
<span data-ttu-id="9ef1f-150">Anger sökvägen till en JSON-formaterad parameter fil.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="9ef1f-151">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="9ef1f-151">-Parameters</span></span>
<span data-ttu-id="9ef1f-152">Anger ett samlings objekt för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="9ef1f-153">Ange en hash-tabell, en ord lista \< \> eller en ord lista \< , WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="9ef1f-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="9ef1f-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef1f-154">-ResourceGroupName</span></span>
<span data-ttu-id="9ef1f-155">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9ef1f-156">-State</span><span class="sxs-lookup"><span data-stu-id="9ef1f-156">-State</span></span>
<span data-ttu-id="9ef1f-157">Anger tillståndet för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="9ef1f-158">De acceptabla värdena för den här parametern är: Enabled och disabled.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="9ef1f-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9ef1f-159">-Confirm</span></span>
<span data-ttu-id="9ef1f-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef1f-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ef1f-161">-WhatIf</span></span>
<span data-ttu-id="9ef1f-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef1f-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef1f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef1f-164">CommonParameters</span></span>
<span data-ttu-id="9ef1f-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef1f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef1f-166">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ef1f-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef1f-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ef1f-167">INPUTS</span></span>

### <span data-ttu-id="9ef1f-168">System. String</span><span class="sxs-lookup"><span data-stu-id="9ef1f-168">System.String</span></span>

## <span data-ttu-id="9ef1f-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ef1f-169">OUTPUTS</span></span>

### <span data-ttu-id="9ef1f-170">System. Object</span><span class="sxs-lookup"><span data-stu-id="9ef1f-170">System.Object</span></span>

## <span data-ttu-id="9ef1f-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ef1f-171">NOTES</span></span>

## <span data-ttu-id="9ef1f-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ef1f-172">RELATED LINKS</span></span>

[<span data-ttu-id="9ef1f-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ef1f-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="9ef1f-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ef1f-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="9ef1f-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ef1f-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="9ef1f-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9ef1f-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


