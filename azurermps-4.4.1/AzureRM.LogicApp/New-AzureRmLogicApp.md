---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
ms.openlocfilehash: 990423db13f13f18f10fb768ac55d2e59b4f2baf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586499"
---
# <span data-ttu-id="d5e53-101">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d5e53-101">New-AzureRmLogicApp</span></span>

## <span data-ttu-id="d5e53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5e53-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e53-103">Skapar ett logiskt program i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d5e53-103">Creates a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5e53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5e53-104">SYNTAX</span></span>

### <span data-ttu-id="d5e53-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5e53-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5e53-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5e53-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5e53-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5e53-107">DESCRIPTION</span></span>
<span data-ttu-id="d5e53-108">Cmdleten **New-AzureRmLogicApp** skapar ett logiskt program med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="d5e53-108">The **New-AzureRmLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="d5e53-109">Ett logiskt program är en samling åtgärder eller utlösare definierade i logik program definition.</span><span class="sxs-lookup"><span data-stu-id="d5e53-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="d5e53-110">Denna cmdlet returnerar ett **arbets flödes** objekt.</span><span class="sxs-lookup"><span data-stu-id="d5e53-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="d5e53-111">Du kan skapa en logik-app genom att ange namn, plats, logik program definition, resurs grupp och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="d5e53-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="d5e53-112">En logik program definition och parametrar är formaterade i Java Script Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="d5e53-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="d5e53-113">Du kan använda ett logik program som mall för definitioner och parametrar.</span><span class="sxs-lookup"><span data-stu-id="d5e53-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="d5e53-114">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="d5e53-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d5e53-115">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="d5e53-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d5e53-116">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="d5e53-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d5e53-117">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="d5e53-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="d5e53-118">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="d5e53-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="d5e53-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5e53-119">EXAMPLES</span></span>

### <span data-ttu-id="d5e53-120">Exempel 1: skapa ett logiskt program med hjälp av definitions-och parameter fil Sök vägar</span><span class="sxs-lookup"><span data-stu-id="d5e53-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
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

<span data-ttu-id="d5e53-121">Det här kommandot skapar ett logiskt program i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d5e53-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="d5e53-122">Programmet logik innehåller definitionen och parametrarna som anges i fil Sök vägar.</span><span class="sxs-lookup"><span data-stu-id="d5e53-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="d5e53-123">Exempel 2: skapa ett logiskt program med hjälp av definitions-och parameter objekt</span><span class="sxs-lookup"><span data-stu-id="d5e53-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
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

<span data-ttu-id="d5e53-124">Det här kommandot skapar ett logiskt program i den angivna resurs gruppen resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d5e53-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="d5e53-125">Exempel 3: skapa ett logiskt program med hjälp av pipeline för att ange resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="d5e53-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzureRmLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
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

<span data-ttu-id="d5e53-126">Det här kommandot får resurs gruppen "ResourceGroup11" genom att använda Get-AzureRmResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5e53-126">This command gets the resource group named ResourceGroup11 by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="d5e53-127">Kommandot överför den resurs gruppen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="d5e53-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d5e53-128">Den aktuella cmdleten skapar ett logiskt program i den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d5e53-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="d5e53-129">Programmet logik innehåller definitionen och parametrarna som anges i fil Sök vägar.</span><span class="sxs-lookup"><span data-stu-id="d5e53-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="d5e53-130">Exempel 4: skapa ett logiskt program baserat på ett befintligt logiskt program</span><span class="sxs-lookup"><span data-stu-id="d5e53-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
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

<span data-ttu-id="d5e53-131">Det första kommandot får till gång till logik programmet med namnet LogicApp03 med hjälp av Get-AzureRmLogicApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5e53-131">The first command gets the logic app named LogicApp03 by using the Get-AzureRmLogicApp cmdlet.</span></span>
<span data-ttu-id="d5e53-132">Kommandot lagrar programmet logik i $Workflow variabel.</span><span class="sxs-lookup"><span data-stu-id="d5e53-132">The command stores the logic app in the $Workflow variable.</span></span>

<span data-ttu-id="d5e53-133">Det andra kommandot skapar ett nytt logiskt program som använder definitionen och parametrarna för logik programmet som lagras i $Workflow.</span><span class="sxs-lookup"><span data-stu-id="d5e53-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="d5e53-134">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5e53-134">PARAMETERS</span></span>

### <span data-ttu-id="d5e53-135">-Definition</span><span class="sxs-lookup"><span data-stu-id="d5e53-135">-Definition</span></span>
<span data-ttu-id="d5e53-136">Anger definitionen för din logik-app som ett objekt eller en sträng i JSON-objekt (Notataion).</span><span class="sxs-lookup"><span data-stu-id="d5e53-136">Specifies the definition for your logic app as an object or a string in JavaScript Object Notataion (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e53-137">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="d5e53-137">-DefinitionFilePath</span></span>
<span data-ttu-id="d5e53-138">Anger definitionen för en logik-app som sökväg till en definitions fil i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="d5e53-138">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e53-139">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="d5e53-139">-IntegrationAccountId</span></span>
<span data-ttu-id="d5e53-140">Anger ett integrerings konto-ID för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="d5e53-140">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="d5e53-141">-Plats</span><span class="sxs-lookup"><span data-stu-id="d5e53-141">-Location</span></span>
<span data-ttu-id="d5e53-142">Anger platsen för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="d5e53-142">Specifies the location of the logic app.</span></span>
<span data-ttu-id="d5e53-143">Ange en plats för Azure Data Center, till exempel West US eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="d5e53-143">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="d5e53-144">Du kan placera ett logiskt program på valfri plats.</span><span class="sxs-lookup"><span data-stu-id="d5e53-144">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="d5e53-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5e53-145">-Name</span></span>
<span data-ttu-id="d5e53-146">Anger namnet på logik programmet.</span><span class="sxs-lookup"><span data-stu-id="d5e53-146">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="d5e53-147">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="d5e53-147">-ParameterFilePath</span></span>
<span data-ttu-id="d5e53-148">Anger sökvägen till en JSON-formaterad parameter fil.</span><span class="sxs-lookup"><span data-stu-id="d5e53-148">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="d5e53-149">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="d5e53-149">-Parameters</span></span>
<span data-ttu-id="d5e53-150">Anger ett samlings objekt för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="d5e53-150">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="d5e53-151">Ange en hash-tabell, en ord lista \<string\> eller en ord lista \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="d5e53-151">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="d5e53-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e53-152">-ResourceGroupName</span></span>
<span data-ttu-id="d5e53-153">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d5e53-153">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d5e53-154">-State</span><span class="sxs-lookup"><span data-stu-id="d5e53-154">-State</span></span>
<span data-ttu-id="d5e53-155">Anger tillståndet för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="d5e53-155">Specifies the state of the logic app.</span></span>
<span data-ttu-id="d5e53-156">De acceptabla värdena för den här parametern är: Enabled och disabled.</span><span class="sxs-lookup"><span data-stu-id="d5e53-156">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="d5e53-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5e53-157">-Confirm</span></span>
<span data-ttu-id="d5e53-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5e53-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5e53-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5e53-159">-WhatIf</span></span>
<span data-ttu-id="d5e53-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5e53-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5e53-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5e53-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5e53-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e53-162">-DefaultProfile</span></span>
<span data-ttu-id="d5e53-163">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5e53-163">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e53-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e53-164">CommonParameters</span></span>
<span data-ttu-id="d5e53-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5e53-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e53-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e53-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e53-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5e53-167">INPUTS</span></span>

### <span data-ttu-id="d5e53-168">Ingen</span><span class="sxs-lookup"><span data-stu-id="d5e53-168">None</span></span>

## <span data-ttu-id="d5e53-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5e53-169">OUTPUTS</span></span>

### <span data-ttu-id="d5e53-170">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="d5e53-170">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="d5e53-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5e53-171">NOTES</span></span>

## <span data-ttu-id="d5e53-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5e53-172">RELATED LINKS</span></span>

[<span data-ttu-id="d5e53-173">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d5e53-173">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="d5e53-174">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d5e53-174">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="d5e53-175">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d5e53-175">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="d5e53-176">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d5e53-176">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


