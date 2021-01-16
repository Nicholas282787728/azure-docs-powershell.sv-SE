---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390636"
---
# <span data-ttu-id="13422-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="13422-101">Update-AzSignalR</span></span>

## <span data-ttu-id="13422-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13422-102">SYNOPSIS</span></span>
<span data-ttu-id="13422-103">Uppdatera en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="13422-103">Update a SignalR service.</span></span>

## <span data-ttu-id="13422-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13422-104">SYNTAX</span></span>

### <span data-ttu-id="13422-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="13422-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13422-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13422-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13422-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13422-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13422-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13422-108">DESCRIPTION</span></span>
<span data-ttu-id="13422-109">Uppdatera en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="13422-109">Update a SignalR service.</span></span>
<span data-ttu-id="13422-110">Följande värden används för parametrar om de inte anges:</span><span class="sxs-lookup"><span data-stu-id="13422-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="13422-111">`ResourceGroupName`: standard resurs gruppen som anges av `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="13422-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="13422-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="13422-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="13422-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13422-113">EXAMPLES</span></span>

### <span data-ttu-id="13422-114">Uppdatera en specifik signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="13422-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="13422-115">Ange ServiceMode och AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="13422-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="13422-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13422-116">PARAMETERS</span></span>

### <span data-ttu-id="13422-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="13422-117">-AllowedOrigin</span></span>
<span data-ttu-id="13422-118">Tillåtna ursprung för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="13422-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="13422-119">För att tillåta alla, Använd "\*" och ta bort alla andra ursprung från listan.</span><span class="sxs-lookup"><span data-stu-id="13422-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="13422-120">Snedstreck tillåts inte som en del av en domän eller efter TOPPnivå</span><span class="sxs-lookup"><span data-stu-id="13422-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="13422-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13422-121">-AsJob</span></span>
<span data-ttu-id="13422-122">Kör cmdleten i bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="13422-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="13422-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13422-123">-DefaultProfile</span></span>
<span data-ttu-id="13422-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13422-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13422-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13422-125">-InputObject</span></span>
<span data-ttu-id="13422-126">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="13422-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="13422-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="13422-127">-Name</span></span>
<span data-ttu-id="13422-128">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="13422-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="13422-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13422-129">-ResourceGroupName</span></span>
<span data-ttu-id="13422-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="13422-130">The resource group name.</span></span>
<span data-ttu-id="13422-131">Standard alternativet används om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="13422-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="13422-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13422-132">-ResourceId</span></span>
<span data-ttu-id="13422-133">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="13422-133">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="13422-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="13422-134">-ServiceMode</span></span>
<span data-ttu-id="13422-135">Tjänst läget för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="13422-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="13422-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="13422-136">-Sku</span></span>
<span data-ttu-id="13422-137">Tjänsten för avsändnings tjänster.</span><span class="sxs-lookup"><span data-stu-id="13422-137">The SignalR service SKU.</span></span>
<span data-ttu-id="13422-138">Standard till "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="13422-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="13422-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="13422-139">-Tag</span></span>
<span data-ttu-id="13422-140">Taggarna för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="13422-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="13422-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="13422-141">-UnitCount</span></span>
<span data-ttu-id="13422-142">Signal tjänstens enheter räknas bara från {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="13422-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="13422-143">Standardvärdet 1.</span><span class="sxs-lookup"><span data-stu-id="13422-143">Default to 1.</span></span>

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

### <span data-ttu-id="13422-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="13422-144">-Confirm</span></span>
<span data-ttu-id="13422-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="13422-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13422-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13422-146">-WhatIf</span></span>
<span data-ttu-id="13422-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="13422-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13422-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="13422-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13422-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13422-149">CommonParameters</span></span>
<span data-ttu-id="13422-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13422-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13422-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13422-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13422-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13422-152">INPUTS</span></span>

### <span data-ttu-id="13422-153">System. String</span><span class="sxs-lookup"><span data-stu-id="13422-153">System.String</span></span>

### <span data-ttu-id="13422-154">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="13422-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="13422-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13422-155">OUTPUTS</span></span>

### <span data-ttu-id="13422-156">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="13422-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="13422-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13422-157">NOTES</span></span>

## <span data-ttu-id="13422-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13422-158">RELATED LINKS</span></span>
