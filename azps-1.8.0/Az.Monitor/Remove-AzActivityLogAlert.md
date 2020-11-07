---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 72d5fb7f5af5fb8e6501bfedee55ebe791765715
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915602"
---
# <span data-ttu-id="eadaa-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eadaa-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="eadaa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eadaa-102">SYNOPSIS</span></span>
<span data-ttu-id="eadaa-103">Tar bort en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="eadaa-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="eadaa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eadaa-104">SYNTAX</span></span>

### <span data-ttu-id="eadaa-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eadaa-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eadaa-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="eadaa-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eadaa-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="eadaa-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eadaa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eadaa-108">DESCRIPTION</span></span>
<span data-ttu-id="eadaa-109">Cmdleten **Remove-AzActivityLogAlert** tar bort en aktivitets logg.</span><span class="sxs-lookup"><span data-stu-id="eadaa-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="eadaa-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="eadaa-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="eadaa-111">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="eadaa-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="eadaa-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eadaa-112">EXAMPLES</span></span>

### <span data-ttu-id="eadaa-113">Exempel 1: ta bort en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="eadaa-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="eadaa-114">Tar bort en aktivitets logg varning med namn-och resurs grupp namn som indata.</span><span class="sxs-lookup"><span data-stu-id="eadaa-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="eadaa-115">Exempel 2: ta bort en aktivitets logg varning med en PSActivityLogAlertResource som indata</span><span class="sxs-lookup"><span data-stu-id="eadaa-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="eadaa-116">Tar bort en aktivitets logg varning med en PSActivityLogAlertResource som indata.</span><span class="sxs-lookup"><span data-stu-id="eadaa-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="eadaa-117">Exempel 3: ta bort ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="eadaa-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="eadaa-118">Det här kommandot tar bort ActivityLogAlert med hjälp av ResourceId-parametern från en pipe.</span><span class="sxs-lookup"><span data-stu-id="eadaa-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="eadaa-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eadaa-119">PARAMETERS</span></span>

### <span data-ttu-id="eadaa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eadaa-120">-DefaultProfile</span></span>
<span data-ttu-id="eadaa-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="eadaa-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eadaa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eadaa-122">-InputObject</span></span>
<span data-ttu-id="eadaa-123">Anger egenskapen InputObject Tags för samtalet för att extrahera namnet och resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="eadaa-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="eadaa-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="eadaa-124">-Name</span></span>
<span data-ttu-id="eadaa-125">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="eadaa-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="eadaa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eadaa-126">-ResourceGroupName</span></span>
<span data-ttu-id="eadaa-127">Namnet på resurs gruppen där aviserings resursen finns.</span><span class="sxs-lookup"><span data-stu-id="eadaa-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="eadaa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eadaa-128">-ResourceId</span></span>
<span data-ttu-id="eadaa-129">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="eadaa-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="eadaa-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eadaa-130">-Confirm</span></span>
<span data-ttu-id="eadaa-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eadaa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eadaa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eadaa-132">-WhatIf</span></span>
<span data-ttu-id="eadaa-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eadaa-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eadaa-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eadaa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eadaa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadaa-135">CommonParameters</span></span>
<span data-ttu-id="eadaa-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eadaa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eadaa-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eadaa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadaa-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eadaa-138">INPUTS</span></span>

### <span data-ttu-id="eadaa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="eadaa-139">System.String</span></span>

### <span data-ttu-id="eadaa-140">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="eadaa-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="eadaa-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eadaa-141">OUTPUTS</span></span>

### <span data-ttu-id="eadaa-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eadaa-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="eadaa-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eadaa-143">NOTES</span></span>

## <span data-ttu-id="eadaa-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eadaa-144">RELATED LINKS</span></span>

[<span data-ttu-id="eadaa-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eadaa-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="eadaa-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eadaa-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="eadaa-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eadaa-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="eadaa-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eadaa-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="eadaa-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="eadaa-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="eadaa-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="eadaa-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

