---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 0bcf5c5ccc871867f89687558777c9550a0b9185
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922513"
---
# <span data-ttu-id="98b7d-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98b7d-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="98b7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="98b7d-103">Tar bort en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="98b7d-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="98b7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98b7d-104">SYNTAX</span></span>

### <span data-ttu-id="98b7d-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="98b7d-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b7d-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="98b7d-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b7d-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="98b7d-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98b7d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98b7d-108">DESCRIPTION</span></span>
<span data-ttu-id="98b7d-109">Cmdleten **Remove-AzActivityLogAlert** tar bort en aktivitets logg.</span><span class="sxs-lookup"><span data-stu-id="98b7d-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="98b7d-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="98b7d-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="98b7d-111">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="98b7d-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="98b7d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98b7d-112">EXAMPLES</span></span>

### <span data-ttu-id="98b7d-113">Exempel 1: ta bort en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="98b7d-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="98b7d-114">Tar bort en aktivitets logg varning med namn-och resurs grupp namn som indata.</span><span class="sxs-lookup"><span data-stu-id="98b7d-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="98b7d-115">Exempel 2: ta bort en aktivitets logg varning med en PSActivityLogAlertResource som indata</span><span class="sxs-lookup"><span data-stu-id="98b7d-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="98b7d-116">Tar bort en aktivitets logg varning med en PSActivityLogAlertResource som indata.</span><span class="sxs-lookup"><span data-stu-id="98b7d-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="98b7d-117">Exempel 3: ta bort ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="98b7d-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="98b7d-118">Det här kommandot tar bort ActivityLogAlert med hjälp av ResourceId-parametern från en pipe.</span><span class="sxs-lookup"><span data-stu-id="98b7d-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="98b7d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98b7d-119">PARAMETERS</span></span>

### <span data-ttu-id="98b7d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b7d-120">-DefaultProfile</span></span>
<span data-ttu-id="98b7d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="98b7d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98b7d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98b7d-122">-InputObject</span></span>
<span data-ttu-id="98b7d-123">Anger egenskapen InputObject Tags för samtalet för att extrahera namnet och resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="98b7d-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b7d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="98b7d-124">-Name</span></span>
<span data-ttu-id="98b7d-125">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="98b7d-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b7d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98b7d-126">-ResourceGroupName</span></span>
<span data-ttu-id="98b7d-127">Namnet på resurs gruppen där aviserings resursen finns.</span><span class="sxs-lookup"><span data-stu-id="98b7d-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b7d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98b7d-128">-ResourceId</span></span>
<span data-ttu-id="98b7d-129">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="98b7d-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b7d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98b7d-130">-Confirm</span></span>
<span data-ttu-id="98b7d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98b7d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b7d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b7d-132">-WhatIf</span></span>
<span data-ttu-id="98b7d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98b7d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98b7d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98b7d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b7d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b7d-135">CommonParameters</span></span>
<span data-ttu-id="98b7d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b7d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b7d-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98b7d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b7d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98b7d-138">INPUTS</span></span>

### <span data-ttu-id="98b7d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="98b7d-139">System.String</span></span>

### <span data-ttu-id="98b7d-140">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="98b7d-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="98b7d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98b7d-141">OUTPUTS</span></span>

### <span data-ttu-id="98b7d-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="98b7d-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="98b7d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98b7d-143">NOTES</span></span>

## <span data-ttu-id="98b7d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98b7d-144">RELATED LINKS</span></span>

[<span data-ttu-id="98b7d-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98b7d-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="98b7d-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98b7d-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="98b7d-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98b7d-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="98b7d-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98b7d-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="98b7d-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="98b7d-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="98b7d-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="98b7d-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

