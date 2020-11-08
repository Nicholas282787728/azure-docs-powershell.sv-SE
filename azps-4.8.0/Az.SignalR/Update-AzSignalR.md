---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103496"
---
# <span data-ttu-id="0adf0-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="0adf0-101">Update-AzSignalR</span></span>

## <span data-ttu-id="0adf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0adf0-102">SYNOPSIS</span></span>
<span data-ttu-id="0adf0-103">Uppdatera en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="0adf0-103">Update a SignalR service.</span></span>

## <span data-ttu-id="0adf0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0adf0-104">SYNTAX</span></span>

### <span data-ttu-id="0adf0-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0adf0-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0adf0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0adf0-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0adf0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0adf0-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0adf0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0adf0-108">DESCRIPTION</span></span>
<span data-ttu-id="0adf0-109">Uppdatera en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="0adf0-109">Update a SignalR service.</span></span>
<span data-ttu-id="0adf0-110">Följande värden används för parametrar om de inte anges:</span><span class="sxs-lookup"><span data-stu-id="0adf0-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="0adf0-111">`ResourceGroupName`: standard resurs gruppen som anges av `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="0adf0-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="0adf0-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="0adf0-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="0adf0-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0adf0-113">EXAMPLES</span></span>

### <span data-ttu-id="0adf0-114">Uppdatera en specifik signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="0adf0-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="0adf0-115">Ange ServiceMode och AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="0adf0-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="0adf0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0adf0-116">PARAMETERS</span></span>

### <span data-ttu-id="0adf0-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="0adf0-117">-AllowedOrigin</span></span>
<span data-ttu-id="0adf0-118">Tillåtna ursprung för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0adf0-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="0adf0-119">För att tillåta alla, Använd "\*" och ta bort alla andra ursprung från listan.</span><span class="sxs-lookup"><span data-stu-id="0adf0-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="0adf0-120">Snedstreck tillåts inte som en del av en domän eller efter TOPPnivå</span><span class="sxs-lookup"><span data-stu-id="0adf0-120">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0adf0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0adf0-121">-AsJob</span></span>
<span data-ttu-id="0adf0-122">Kör cmdleten i bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="0adf0-122">Run the cmdlet in background job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0adf0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0adf0-123">-DefaultProfile</span></span>
<span data-ttu-id="0adf0-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0adf0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0adf0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0adf0-125">-InputObject</span></span>
<span data-ttu-id="0adf0-126">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="0adf0-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0adf0-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="0adf0-127">-Name</span></span>
<span data-ttu-id="0adf0-128">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="0adf0-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0adf0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0adf0-129">-ResourceGroupName</span></span>
<span data-ttu-id="0adf0-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0adf0-130">The resource group name.</span></span>
<span data-ttu-id="0adf0-131">Standard alternativet används om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="0adf0-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0adf0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0adf0-132">-ResourceId</span></span>
<span data-ttu-id="0adf0-133">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="0adf0-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0adf0-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="0adf0-134">-ServiceMode</span></span>
<span data-ttu-id="0adf0-135">Tjänst läget för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0adf0-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="0adf0-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="0adf0-136">-Sku</span></span>
<span data-ttu-id="0adf0-137">Tjänsten för avsändnings tjänster.</span><span class="sxs-lookup"><span data-stu-id="0adf0-137">The SignalR service SKU.</span></span>
<span data-ttu-id="0adf0-138">Standard till "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="0adf0-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="0adf0-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0adf0-139">-Tag</span></span>
<span data-ttu-id="0adf0-140">Taggarna för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0adf0-140">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0adf0-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="0adf0-141">-UnitCount</span></span>
<span data-ttu-id="0adf0-142">Signal tjänstens enheter räknas bara från {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="0adf0-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="0adf0-143">Standardvärdet 1.</span><span class="sxs-lookup"><span data-stu-id="0adf0-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0adf0-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0adf0-144">-Confirm</span></span>
<span data-ttu-id="0adf0-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0adf0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0adf0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0adf0-146">-WhatIf</span></span>
<span data-ttu-id="0adf0-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0adf0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0adf0-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0adf0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0adf0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0adf0-149">CommonParameters</span></span>
<span data-ttu-id="0adf0-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0adf0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0adf0-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0adf0-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0adf0-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0adf0-152">INPUTS</span></span>

### <span data-ttu-id="0adf0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0adf0-153">System.String</span></span>

### <span data-ttu-id="0adf0-154">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="0adf0-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="0adf0-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0adf0-155">OUTPUTS</span></span>

### <span data-ttu-id="0adf0-156">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="0adf0-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="0adf0-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0adf0-157">NOTES</span></span>

## <span data-ttu-id="0adf0-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0adf0-158">RELATED LINKS</span></span>
