---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: 8749744d6ab10ba1b48f7c8e56792c5891edb5eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574852"
---
# <span data-ttu-id="e6919-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e6919-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="e6919-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6919-102">SYNOPSIS</span></span>
<span data-ttu-id="e6919-103">Tar bort en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="e6919-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6919-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6919-104">SYNTAX</span></span>

### <span data-ttu-id="e6919-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e6919-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6919-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e6919-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6919-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6919-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6919-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6919-108">DESCRIPTION</span></span>
<span data-ttu-id="e6919-109">Cmdleten **Remove-AzureRmActivityLogAlert** tar bort en aktivitets logg.</span><span class="sxs-lookup"><span data-stu-id="e6919-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="e6919-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="e6919-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="e6919-111">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="e6919-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e6919-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6919-112">EXAMPLES</span></span>

### <span data-ttu-id="e6919-113">Exempel 1: ta bort en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="e6919-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="e6919-114">Tar bort en aktivitets logg varning med namn-och resurs grupp namn som indata.</span><span class="sxs-lookup"><span data-stu-id="e6919-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="e6919-115">Exempel 2: ta bort en aktivitets logg varning med en PSActivityLogAlertResource som indata</span><span class="sxs-lookup"><span data-stu-id="e6919-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="e6919-116">Tar bort en aktivitets logg varning med en PSActivityLogAlertResource som indata.</span><span class="sxs-lookup"><span data-stu-id="e6919-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="e6919-117">Exempel 3: ta bort ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6919-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="e6919-118">Det här kommandot tar bort ActivityLogAlert med hjälp av ResourceId-parametern från en pipe.</span><span class="sxs-lookup"><span data-stu-id="e6919-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="e6919-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6919-119">PARAMETERS</span></span>

### <span data-ttu-id="e6919-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6919-120">-DefaultProfile</span></span>
<span data-ttu-id="e6919-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e6919-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6919-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6919-122">-InputObject</span></span>
<span data-ttu-id="e6919-123">Anger egenskapen InputObject Tags för samtalet för att extrahera namnet och resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e6919-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="e6919-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6919-124">-Name</span></span>
<span data-ttu-id="e6919-125">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="e6919-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="e6919-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6919-126">-ResourceGroupName</span></span>
<span data-ttu-id="e6919-127">Namnet på resurs gruppen där aviserings resursen finns.</span><span class="sxs-lookup"><span data-stu-id="e6919-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="e6919-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6919-128">-ResourceId</span></span>
<span data-ttu-id="e6919-129">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="e6919-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="e6919-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6919-130">-Confirm</span></span>
<span data-ttu-id="e6919-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6919-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6919-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6919-132">-WhatIf</span></span>
<span data-ttu-id="e6919-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6919-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6919-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6919-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6919-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6919-135">CommonParameters</span></span>
<span data-ttu-id="e6919-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6919-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6919-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6919-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6919-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6919-138">INPUTS</span></span>

### <span data-ttu-id="e6919-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e6919-139">System.String</span></span>

### <span data-ttu-id="e6919-140">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e6919-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="e6919-141">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e6919-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e6919-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6919-142">OUTPUTS</span></span>

### <span data-ttu-id="e6919-143">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e6919-143">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e6919-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6919-144">NOTES</span></span>

## <span data-ttu-id="e6919-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6919-145">RELATED LINKS</span></span>

[<span data-ttu-id="e6919-146">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e6919-146">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e6919-147">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e6919-147">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e6919-148">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e6919-148">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e6919-149">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e6919-149">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e6919-150">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e6919-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="e6919-151">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e6919-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

