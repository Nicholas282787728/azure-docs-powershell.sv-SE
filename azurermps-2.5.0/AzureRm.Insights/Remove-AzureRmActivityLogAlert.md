---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 1dfd435d2797ee7430349546a5d2ba6fa2fe0023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929901"
---
# <span data-ttu-id="f2dc6-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2dc6-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="f2dc6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="f2dc6-103">Tar bort en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2dc6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2dc6-104">SYNTAX</span></span>

### <span data-ttu-id="f2dc6-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f2dc6-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2dc6-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2dc6-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2dc6-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2dc6-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2dc6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2dc6-108">DESCRIPTION</span></span>
<span data-ttu-id="f2dc6-109">Cmdleten **Remove-AzureRmActivityLogAlert** tar bort en aktivitets logg.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="f2dc6-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="f2dc6-111">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f2dc6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2dc6-112">EXAMPLES</span></span>

### <span data-ttu-id="f2dc6-113">Exempel 1: ta bort en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="f2dc6-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="f2dc6-114">Tar bort en aktivitets logg varning med namn-och resurs grupp namn som indata.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="f2dc6-115">Exempel 2: ta bort en aktivitets logg varning med en PSActivityLogAlertResource som indata</span><span class="sxs-lookup"><span data-stu-id="f2dc6-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="f2dc6-116">Tar bort en aktivitets logg varning med en PSActivityLogAlertResource som indata.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="f2dc6-117">Exempel 3: ta bort ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2dc6-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="f2dc6-118">Det här kommandot tar bort ActivityLogAlert med hjälp av ResourceId-parametern från en pipe.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="f2dc6-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2dc6-119">PARAMETERS</span></span>

### <span data-ttu-id="f2dc6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2dc6-120">-DefaultProfile</span></span>
<span data-ttu-id="f2dc6-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f2dc6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2dc6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2dc6-122">-InputObject</span></span>
<span data-ttu-id="f2dc6-123">Anger egenskapen InputObject Tags för samtalet för att extrahera namnet och resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="f2dc6-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2dc6-124">-Name</span></span>
<span data-ttu-id="f2dc6-125">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="f2dc6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2dc6-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2dc6-127">Namnet på resurs gruppen där aviserings resursen finns.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="f2dc6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2dc6-128">-ResourceId</span></span>
<span data-ttu-id="f2dc6-129">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="f2dc6-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2dc6-130">-Confirm</span></span>
<span data-ttu-id="f2dc6-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2dc6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2dc6-132">-WhatIf</span></span>
<span data-ttu-id="f2dc6-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2dc6-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2dc6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2dc6-135">CommonParameters</span></span>
<span data-ttu-id="f2dc6-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2dc6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2dc6-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2dc6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2dc6-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2dc6-138">INPUTS</span></span>

### <span data-ttu-id="f2dc6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f2dc6-139">System.String</span></span>

### <span data-ttu-id="f2dc6-140">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="f2dc6-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="f2dc6-141">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2dc6-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f2dc6-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2dc6-142">OUTPUTS</span></span>

### <span data-ttu-id="f2dc6-143">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f2dc6-143">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="f2dc6-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2dc6-144">NOTES</span></span>

## <span data-ttu-id="f2dc6-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2dc6-145">RELATED LINKS</span></span>

[<span data-ttu-id="f2dc6-146">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2dc6-146">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f2dc6-147">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2dc6-147">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f2dc6-148">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2dc6-148">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f2dc6-149">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f2dc6-149">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f2dc6-150">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="f2dc6-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="f2dc6-151">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="f2dc6-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

