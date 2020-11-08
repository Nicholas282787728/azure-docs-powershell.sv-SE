---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 39f097c2cc580d2b161e3b4b31b247c13c3a411c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092737"
---
# <span data-ttu-id="1d963-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1d963-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="1d963-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d963-102">SYNOPSIS</span></span>
<span data-ttu-id="1d963-103">Aktiverar en aktivitets logg varning och anger dess taggar.</span><span class="sxs-lookup"><span data-stu-id="1d963-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="1d963-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d963-104">SYNTAX</span></span>

### <span data-ttu-id="1d963-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1d963-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d963-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d963-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d963-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d963-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d963-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d963-108">DESCRIPTION</span></span>
<span data-ttu-id="1d963-109">Med cmdleten **Enable-AzActivityLogAlert** kan du aktivera en aktivitets loggs avisering och ange dess taggar.</span><span class="sxs-lookup"><span data-stu-id="1d963-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="1d963-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="1d963-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="1d963-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d963-111">EXAMPLES</span></span>

### <span data-ttu-id="1d963-112">Exempel 1: Aktivera en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="1d963-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="1d963-113">Det här kommandot aktiverar aviseringen för aktivitets loggen med namnet alert1 i resurs gruppen standard-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="1d963-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="1d963-114">Exempel 2: Aktivera en aktivitets logg varning med ett PSActivityLogAlertResource-objekt som inmatning</span><span class="sxs-lookup"><span data-stu-id="1d963-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="1d963-115">Det här kommandot aktiverar en aktivitets loggs avisering med namnet alert1.</span><span class="sxs-lookup"><span data-stu-id="1d963-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="1d963-116">För den här funktionen används ett PSActivityLogAlertResource-objekt som indataargument.</span><span class="sxs-lookup"><span data-stu-id="1d963-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="1d963-117">Exempel 3: Aktivera ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d963-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="1d963-118">Det här kommandot aktiverar ActivityLogAlert med hjälp av parametern ResourceId från pipe.</span><span class="sxs-lookup"><span data-stu-id="1d963-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="1d963-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d963-119">PARAMETERS</span></span>

### <span data-ttu-id="1d963-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d963-120">-DefaultProfile</span></span>
<span data-ttu-id="1d963-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1d963-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d963-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d963-122">-InputObject</span></span>
<span data-ttu-id="1d963-123">Anger egenskapen InputObject Tags för samtalet för att extrahera obligatoriskt namn, resurs grupp namn och valfria egenskaper.</span><span class="sxs-lookup"><span data-stu-id="1d963-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d963-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1d963-124">-Name</span></span>
<span data-ttu-id="1d963-125">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="1d963-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d963-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d963-126">-ResourceGroupName</span></span>
<span data-ttu-id="1d963-127">Namnet på resurs gruppen där aviserings resursen ska finnas.</span><span class="sxs-lookup"><span data-stu-id="1d963-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d963-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d963-128">-ResourceId</span></span>
<span data-ttu-id="1d963-129">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="1d963-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d963-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d963-130">-Confirm</span></span>
<span data-ttu-id="1d963-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d963-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d963-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d963-132">-WhatIf</span></span>
<span data-ttu-id="1d963-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d963-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d963-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d963-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d963-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d963-135">CommonParameters</span></span>
<span data-ttu-id="1d963-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d963-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d963-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d963-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d963-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d963-138">INPUTS</span></span>

### <span data-ttu-id="1d963-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1d963-139">System.String</span></span>

### <span data-ttu-id="1d963-140">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="1d963-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="1d963-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d963-141">OUTPUTS</span></span>

### <span data-ttu-id="1d963-142">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="1d963-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="1d963-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d963-143">NOTES</span></span>

## <span data-ttu-id="1d963-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d963-144">RELATED LINKS</span></span>

[<span data-ttu-id="1d963-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1d963-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="1d963-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1d963-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="1d963-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1d963-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="1d963-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1d963-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="1d963-149">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="1d963-149">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="1d963-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1d963-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
