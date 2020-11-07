---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: adff43beed709db91b2f22bd1072728d3e7a0425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758404"
---
# <span data-ttu-id="a67ed-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a67ed-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="a67ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a67ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a67ed-103">Tar bort en aktivitets loggs avisering.</span><span class="sxs-lookup"><span data-stu-id="a67ed-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a67ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a67ed-104">SYNTAX</span></span>

### <span data-ttu-id="a67ed-105">Standard parametrar för att ta bort en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="a67ed-105">Default parameters for remove an activity log alert</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a67ed-106">Parametrar för att ta bort en aktivitets logg meddelanden som tar ett värde från en pipe</span><span class="sxs-lookup"><span data-stu-id="a67ed-106">Parameters to remove an activity log alerts taking value from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a67ed-107">Parametrar för att ta bort en aktivitets logg meddelanden som tar värdet av ResourceId från pipe</span><span class="sxs-lookup"><span data-stu-id="a67ed-107">Parameters to remove an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a67ed-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a67ed-108">DESCRIPTION</span></span>
<span data-ttu-id="a67ed-109">Cmdleten **Remove-AzureRmActivityLogAlert** tar bort en aktivitets logg.</span><span class="sxs-lookup"><span data-stu-id="a67ed-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="a67ed-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="a67ed-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="a67ed-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a67ed-111">EXAMPLES</span></span>

### <span data-ttu-id="a67ed-112">Exempel 1: ta bort en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="a67ed-112">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="a67ed-113">Tar bort en aktivitets logg varning med namn-och resurs grupp namn som indata.</span><span class="sxs-lookup"><span data-stu-id="a67ed-113">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="a67ed-114">Exempel 2: ta bort en aktivitets logg varning med en PSActivityLogAlertResource som indata</span><span class="sxs-lookup"><span data-stu-id="a67ed-114">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="a67ed-115">Tar bort en aktivitets logg varning med en PSActivityLogAlertResource som indata.</span><span class="sxs-lookup"><span data-stu-id="a67ed-115">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="a67ed-116">Exempel 3: ta bort ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="a67ed-116">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="a67ed-117">Det här kommandot tar bort ActivityLogAlert med hjälp av ResourceId-parametern från en pipe.</span><span class="sxs-lookup"><span data-stu-id="a67ed-117">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="a67ed-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a67ed-118">PARAMETERS</span></span>

### <span data-ttu-id="a67ed-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a67ed-119">-Name</span></span>
<span data-ttu-id="a67ed-120">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="a67ed-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a67ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a67ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="a67ed-122">Namnet på resurs gruppen där aviserings resursen finns.</span><span class="sxs-lookup"><span data-stu-id="a67ed-122">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a67ed-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a67ed-123">-InputObject</span></span>
<span data-ttu-id="a67ed-124">Anger egenskapen InputObject Tags för samtalet för att extrahera namnet och resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a67ed-124">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to remove an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a67ed-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a67ed-125">-ResourceId</span></span>
<span data-ttu-id="a67ed-126">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a67ed-126">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to remove an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a67ed-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a67ed-127">-Confirm</span></span>
<span data-ttu-id="a67ed-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a67ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a67ed-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a67ed-129">-DefaultProfile</span></span>
<span data-ttu-id="a67ed-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a67ed-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a67ed-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a67ed-131">-WhatIf</span></span>
<span data-ttu-id="a67ed-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a67ed-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a67ed-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a67ed-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a67ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a67ed-134">CommonParameters</span></span>
<span data-ttu-id="a67ed-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a67ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a67ed-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a67ed-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a67ed-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a67ed-137">INPUTS</span></span>

## <span data-ttu-id="a67ed-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a67ed-138">OUTPUTS</span></span>

### <span data-ttu-id="a67ed-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a67ed-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="a67ed-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a67ed-140">NOTES</span></span>

## <span data-ttu-id="a67ed-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a67ed-141">RELATED LINKS</span></span>

[<span data-ttu-id="a67ed-142">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a67ed-142">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a67ed-143">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a67ed-143">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a67ed-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a67ed-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a67ed-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a67ed-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a67ed-146">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a67ed-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="a67ed-147">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a67ed-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

