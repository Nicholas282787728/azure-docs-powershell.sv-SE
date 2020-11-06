---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 66c127e701432604654cacb556d71588d9786dbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574288"
---
# <span data-ttu-id="be27a-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="be27a-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="be27a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be27a-102">SYNOPSIS</span></span>
<span data-ttu-id="be27a-103">Skapar en ny eller anger en befintlig aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="be27a-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be27a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be27a-104">SYNTAX</span></span>

### <span data-ttu-id="be27a-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be27a-105">SetByNameAndResourceGroup</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be27a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="be27a-106">SetByResourceId</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be27a-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="be27a-107">SetByInputObject</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be27a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be27a-108">DESCRIPTION</span></span>
<span data-ttu-id="be27a-109">Cmdleten **set-AzureRmActivityLogAlert** skapar en ny eller anger en befintlig varning för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="be27a-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="be27a-110">För taggar, villkor och åtgärder måste objekten skapas i förväg och skickas som en kommaseparerad (se exemplet nedan).</span><span class="sxs-lookup"><span data-stu-id="be27a-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="be27a-111">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan den faktiskt skapar/ändrar resursen.</span><span class="sxs-lookup"><span data-stu-id="be27a-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

<span data-ttu-id="be27a-112">**Obs!** den här cmdleten och dess relaterade ersättare (november 2017) **AzureRmLogAlertRule**.</span><span class="sxs-lookup"><span data-stu-id="be27a-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzureRmLogAlertRule**.</span></span>

## <span data-ttu-id="be27a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be27a-113">EXAMPLES</span></span>

### <span data-ttu-id="be27a-114">Exempel 1: skapa en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="be27a-114">Example 1: Create an Activity Log Alert</span></span>
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

<span data-ttu-id="be27a-115">De första fyra kommandona skapar ett löv villkor och en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="be27a-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="be27a-116">Med kommandot slut skapas en aktivitets logg varning med hjälp av villkoret och åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="be27a-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="be27a-117">Exempel 2: skapa en aktivitets logg varning inaktive rad</span><span class="sxs-lookup"><span data-stu-id="be27a-117">Example 2: Create an Activity Log Alert disabled</span></span>
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

<span data-ttu-id="be27a-118">De första fyra kommandona skapar ett löv villkor och en åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="be27a-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="be27a-119">Med kommandot slutgiltig skapar du en aktivitets logg varning med hjälp av villkoret och åtgärds gruppen, men aviseringen för inaktive ring.</span><span class="sxs-lookup"><span data-stu-id="be27a-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="be27a-120">Exempel 3: Ange en aktivitets logg varning baserat på ett värde från en pipe eller en InputObject-parameter</span><span class="sxs-lookup"><span data-stu-id="be27a-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="be27a-121">Det första kommandot påminner om en NOP, den ställer in en varning med samma värden som den redan innehåller resten av kommandona hämtar notifieringsregeln, ändrar beskrivningen och inaktiverar den och använder sedan parametern InputObject för att spara ändringarna</span><span class="sxs-lookup"><span data-stu-id="be27a-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="be27a-122">Exempel 4: Ange en aktivitets loggs varning baserat på värdet ResourceId från pipe</span><span class="sxs-lookup"><span data-stu-id="be27a-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="be27a-123">Om den angivna logg varnings regeln finns i det här kommandot inaktive ras den.</span><span class="sxs-lookup"><span data-stu-id="be27a-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="be27a-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be27a-124">PARAMETERS</span></span>

### <span data-ttu-id="be27a-125">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="be27a-125">-Action</span></span>
<span data-ttu-id="be27a-126">Listan med åtgärds grupper för varningen för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="be27a-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="be27a-127">-Villkor</span><span class="sxs-lookup"><span data-stu-id="be27a-127">-Condition</span></span>
<span data-ttu-id="be27a-128">Listan med villkor för aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="be27a-128">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="be27a-129">**Obs!** i listan med villkor måste det finnas minst ett med fältet lika med "kategori".</span><span class="sxs-lookup"><span data-stu-id="be27a-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="be27a-130">Server delen reagerar med 400 (BadRequest) om det här villkoret inte är tillgängligt.</span><span class="sxs-lookup"><span data-stu-id="be27a-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="be27a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be27a-131">-DefaultProfile</span></span>
<span data-ttu-id="be27a-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="be27a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-133">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="be27a-133">-Description</span></span>
<span data-ttu-id="be27a-134">Beskrivning av aviserings resursen.</span><span class="sxs-lookup"><span data-stu-id="be27a-134">The description of the alert resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="be27a-135">-DisableAlert</span></span>
<span data-ttu-id="be27a-136">Gör det möjligt för användaren att skapa en inaktive rad aktivitets logg varning.</span><span class="sxs-lookup"><span data-stu-id="be27a-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="be27a-137">Om det inte anges skapas notifieringar aktiverat.</span><span class="sxs-lookup"><span data-stu-id="be27a-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be27a-138">-InputObject</span></span>
<span data-ttu-id="be27a-139">Anger egenskapen InputObject Tags för samtalet för att extrahera namnet och resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="be27a-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="be27a-140">-Location</span></span>
<span data-ttu-id="be27a-141">Platsen där aviseringen för aktivitets loggen finns.</span><span class="sxs-lookup"><span data-stu-id="be27a-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="be27a-142">-Name</span></span>
<span data-ttu-id="be27a-143">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="be27a-143">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be27a-144">-ResourceGroupName</span></span>
<span data-ttu-id="be27a-145">Namnet på resurs gruppen där aviserings resursen ska finnas.</span><span class="sxs-lookup"><span data-stu-id="be27a-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be27a-146">-ResourceId</span></span>
<span data-ttu-id="be27a-147">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="be27a-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-148">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="be27a-148">-Scope</span></span>
<span data-ttu-id="be27a-149">Listan med omfattningar för aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="be27a-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="be27a-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="be27a-150">-Tag</span></span>
<span data-ttu-id="be27a-151">Anger egenskapen Tags för aviserings resursen aktivitets logg.</span><span class="sxs-lookup"><span data-stu-id="be27a-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="be27a-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="be27a-152">-Confirm</span></span>
<span data-ttu-id="be27a-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="be27a-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be27a-154">-WhatIf</span></span>
<span data-ttu-id="be27a-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="be27a-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be27a-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="be27a-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be27a-157">CommonParameters</span></span>
<span data-ttu-id="be27a-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be27a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be27a-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be27a-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be27a-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be27a-160">INPUTS</span></span>

### <span data-ttu-id="be27a-161">Ingen</span><span class="sxs-lookup"><span data-stu-id="be27a-161">None</span></span>
<span data-ttu-id="be27a-162">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="be27a-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be27a-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be27a-163">OUTPUTS</span></span>

### <span data-ttu-id="be27a-164">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="be27a-164">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="be27a-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be27a-165">NOTES</span></span>

## <span data-ttu-id="be27a-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be27a-166">RELATED LINKS</span></span>

[<span data-ttu-id="be27a-167">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="be27a-167">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="be27a-168">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="be27a-168">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="be27a-169">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="be27a-169">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="be27a-170">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="be27a-170">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="be27a-171">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="be27a-171">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="be27a-172">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="be27a-172">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
