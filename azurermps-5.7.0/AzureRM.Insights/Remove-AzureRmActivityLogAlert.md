---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: b712363b2b4e1d610f00f1111c48145debe084a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581167"
---
# <span data-ttu-id="ded6d-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ded6d-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="ded6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ded6d-102">SYNOPSIS</span></span>
<span data-ttu-id="ded6d-103">Tar bort en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="ded6d-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ded6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ded6d-104">SYNTAX</span></span>

### <span data-ttu-id="ded6d-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ded6d-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ded6d-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ded6d-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ded6d-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="ded6d-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ded6d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ded6d-108">DESCRIPTION</span></span>
<span data-ttu-id="ded6d-109">Cmdleten **Remove-AzureRmActivityLogAlert** tar bort en aktivitets logg.</span><span class="sxs-lookup"><span data-stu-id="ded6d-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="ded6d-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="ded6d-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

<span data-ttu-id="ded6d-111">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="ded6d-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ded6d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ded6d-112">EXAMPLES</span></span>

### <span data-ttu-id="ded6d-113">Exempel 1: ta bort en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="ded6d-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="ded6d-114">Tar bort en aktivitets logg varning med namn-och resurs grupp namn som indata.</span><span class="sxs-lookup"><span data-stu-id="ded6d-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="ded6d-115">Exempel 2: ta bort en aktivitets logg varning med en PSActivityLogAlertResource som indata</span><span class="sxs-lookup"><span data-stu-id="ded6d-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="ded6d-116">Tar bort en aktivitets logg varning med en PSActivityLogAlertResource som indata.</span><span class="sxs-lookup"><span data-stu-id="ded6d-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="ded6d-117">Exempel 3: ta bort ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="ded6d-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="ded6d-118">Det här kommandot tar bort ActivityLogAlert med hjälp av ResourceId-parametern från en pipe.</span><span class="sxs-lookup"><span data-stu-id="ded6d-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="ded6d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ded6d-119">PARAMETERS</span></span>

### <span data-ttu-id="ded6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded6d-120">-DefaultProfile</span></span>
<span data-ttu-id="ded6d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ded6d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ded6d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ded6d-122">-InputObject</span></span>
<span data-ttu-id="ded6d-123">Anger egenskapen InputObject Tags för samtalet för att extrahera namnet och resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="ded6d-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ded6d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="ded6d-124">-Name</span></span>
<span data-ttu-id="ded6d-125">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="ded6d-125">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ded6d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded6d-126">-ResourceGroupName</span></span>
<span data-ttu-id="ded6d-127">Namnet på resurs gruppen där aviserings resursen finns.</span><span class="sxs-lookup"><span data-stu-id="ded6d-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ded6d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ded6d-128">-ResourceId</span></span>
<span data-ttu-id="ded6d-129">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="ded6d-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ded6d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ded6d-130">-Confirm</span></span>
<span data-ttu-id="ded6d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ded6d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ded6d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ded6d-132">-WhatIf</span></span>
<span data-ttu-id="ded6d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ded6d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ded6d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ded6d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ded6d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded6d-135">CommonParameters</span></span>
<span data-ttu-id="ded6d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded6d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded6d-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded6d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded6d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ded6d-138">INPUTS</span></span>

### <span data-ttu-id="ded6d-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="ded6d-139">None</span></span>
<span data-ttu-id="ded6d-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ded6d-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ded6d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ded6d-141">OUTPUTS</span></span>

### <span data-ttu-id="ded6d-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ded6d-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ded6d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ded6d-143">NOTES</span></span>

## <span data-ttu-id="ded6d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ded6d-144">RELATED LINKS</span></span>

[<span data-ttu-id="ded6d-145">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ded6d-145">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ded6d-146">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ded6d-146">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ded6d-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ded6d-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ded6d-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ded6d-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ded6d-149">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="ded6d-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="ded6d-150">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="ded6d-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

