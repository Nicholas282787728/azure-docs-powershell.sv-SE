---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 993e1b9cde421bad1039f94f4557ee58f781c20b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928854"
---
# <span data-ttu-id="88a03-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88a03-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="88a03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88a03-102">SYNOPSIS</span></span>
<span data-ttu-id="88a03-103">Skapar en ny eller anger en befintlig aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="88a03-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88a03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88a03-104">SYNTAX</span></span>

### <span data-ttu-id="88a03-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88a03-105">SetByNameAndResourceGroup</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88a03-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="88a03-106">SetByResourceId</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88a03-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="88a03-107">SetByInputObject</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88a03-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88a03-108">DESCRIPTION</span></span>
<span data-ttu-id="88a03-109">Cmdleten **set-AzureRmActivityLogAlert** skapar en ny eller anger en befintlig varning för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="88a03-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="88a03-110">För taggar, villkor och åtgärder måste objekten skapas i förväg och skickas som en kommaseparerad (se exemplet nedan).</span><span class="sxs-lookup"><span data-stu-id="88a03-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="88a03-111">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan den faktiskt skapar/ändrar resursen.</span><span class="sxs-lookup"><span data-stu-id="88a03-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="88a03-112">**Obs!** den här cmdleten och dess relaterade ersättare (november 2017) **AzureRmLogAlertRule**.</span><span class="sxs-lookup"><span data-stu-id="88a03-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzureRmLogAlertRule**.</span></span>

## <span data-ttu-id="88a03-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88a03-113">EXAMPLES</span></span>

### <span data-ttu-id="88a03-114">Exempel 1: skapa en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="88a03-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="88a03-115">De första fyra kommandona skapar ett löv villkor och en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="88a03-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="88a03-116">Med kommandot slut skapas en aktivitets logg varning med hjälp av villkoret och åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="88a03-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="88a03-117">Exempel 2: skapa en aktivitets logg varning inaktive rad</span><span class="sxs-lookup"><span data-stu-id="88a03-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="88a03-118">De första fyra kommandona skapar ett löv villkor och en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="88a03-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="88a03-119">Med kommandot slutgiltig skapar du en aktivitets logg varning med hjälp av villkoret och åtgärds gruppen, men aviseringen för inaktive ring.</span><span class="sxs-lookup"><span data-stu-id="88a03-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="88a03-120">Exempel 3: Ange en aktivitets logg varning baserat på ett värde från en pipe eller en InputObject-parameter</span><span class="sxs-lookup"><span data-stu-id="88a03-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="88a03-121">Det första kommandot påminner om en NOP, den ställer in en varning med samma värden som den redan innehåller resten av kommandona hämtar notifieringsregeln, ändrar beskrivningen och inaktiverar den och använder sedan parametern InputObject för att spara ändringarna</span><span class="sxs-lookup"><span data-stu-id="88a03-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="88a03-122">Exempel 4: Ange en aktivitets loggs varning baserat på värdet ResourceId från pipe</span><span class="sxs-lookup"><span data-stu-id="88a03-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="88a03-123">Om den angivna logg varnings regeln finns i det här kommandot inaktive ras den.</span><span class="sxs-lookup"><span data-stu-id="88a03-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="88a03-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88a03-124">PARAMETERS</span></span>

### <span data-ttu-id="88a03-125">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="88a03-125">-Action</span></span>
<span data-ttu-id="88a03-126">Listan med åtgärds grupper för varningen för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="88a03-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-127">-Villkor</span><span class="sxs-lookup"><span data-stu-id="88a03-127">-Condition</span></span>
<span data-ttu-id="88a03-128">Listan med villkor för aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="88a03-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="88a03-129">**Obs!** i listan med villkor måste det finnas minst ett med fältet lika med "kategori".</span><span class="sxs-lookup"><span data-stu-id="88a03-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="88a03-130">Server delen reagerar med 400 (BadRequest) om det här villkoret inte är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="88a03-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a03-131">-DefaultProfile</span></span>
<span data-ttu-id="88a03-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="88a03-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88a03-133">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="88a03-133">-Description</span></span>
<span data-ttu-id="88a03-134">Beskrivning av aviserings resursen.</span><span class="sxs-lookup"><span data-stu-id="88a03-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="88a03-135">-DisableAlert</span></span>
<span data-ttu-id="88a03-136">Gör det möjligt för användaren att skapa en inaktive rad aktivitets logg varning.</span><span class="sxs-lookup"><span data-stu-id="88a03-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="88a03-137">Om det inte anges skapas notifieringar aktiverat.</span><span class="sxs-lookup"><span data-stu-id="88a03-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88a03-138">-InputObject</span></span>
<span data-ttu-id="88a03-139">Anger egenskapen InputObject Tags för samtalet för att extrahera namnet och resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="88a03-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="88a03-140">-Location</span></span>
<span data-ttu-id="88a03-141">Platsen där aviseringen för aktivitets loggen finns.</span><span class="sxs-lookup"><span data-stu-id="88a03-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="88a03-142">-Name</span></span>
<span data-ttu-id="88a03-143">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="88a03-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88a03-144">-ResourceGroupName</span></span>
<span data-ttu-id="88a03-145">Namnet på resurs gruppen där aviserings resursen ska finnas.</span><span class="sxs-lookup"><span data-stu-id="88a03-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88a03-146">-ResourceId</span></span>
<span data-ttu-id="88a03-147">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="88a03-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-148">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="88a03-148">-Scope</span></span>
<span data-ttu-id="88a03-149">Listan med omfattningar för aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="88a03-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="88a03-150">-Tag</span></span>
<span data-ttu-id="88a03-151">Anger egenskapen Tags för aviserings resursen aktivitets logg.</span><span class="sxs-lookup"><span data-stu-id="88a03-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="88a03-152">-Confirm</span></span>
<span data-ttu-id="88a03-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="88a03-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88a03-154">-WhatIf</span></span>
<span data-ttu-id="88a03-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="88a03-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88a03-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="88a03-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a03-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a03-157">CommonParameters</span></span>
<span data-ttu-id="88a03-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88a03-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a03-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a03-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a03-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88a03-160">INPUTS</span></span>

### <span data-ttu-id="88a03-161">System. String</span><span class="sxs-lookup"><span data-stu-id="88a03-161">System.String</span></span>

### <span data-ttu-id="88a03-162">System. Collections. Generic. list ' 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="88a03-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="88a03-163">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertLeafCondition, Microsoft. Azure. commands. Insights, version = 5.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="88a03-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="88a03-164">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitoring. Management. Models. ActivityLogAlertActionGroup, Microsoft. Azure. commands. Insights, version = 5.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="88a03-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="88a03-165">System. Collections. Generic. ordbok ' 2 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089], [system. String, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="88a03-165">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="88a03-166">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="88a03-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="88a03-167">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="88a03-167">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="88a03-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88a03-168">OUTPUTS</span></span>

### <span data-ttu-id="88a03-169">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="88a03-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="88a03-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88a03-170">NOTES</span></span>

## <span data-ttu-id="88a03-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88a03-171">RELATED LINKS</span></span>

[<span data-ttu-id="88a03-172">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88a03-172">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="88a03-173">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88a03-173">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="88a03-174">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88a03-174">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="88a03-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="88a03-175">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="88a03-176">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="88a03-176">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="88a03-177">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="88a03-177">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
