---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103498"
---
# <span data-ttu-id="7097f-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="7097f-101">New-AzSignalR</span></span>

## <span data-ttu-id="7097f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7097f-102">SYNOPSIS</span></span>
<span data-ttu-id="7097f-103">Skapa en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="7097f-103">Create a SignalR service.</span></span>

## <span data-ttu-id="7097f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7097f-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7097f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7097f-105">DESCRIPTION</span></span>
<span data-ttu-id="7097f-106">Skapa en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="7097f-106">Create a SignalR service.</span></span>
<span data-ttu-id="7097f-107">Följande värden används för parametrar om de inte anges:</span><span class="sxs-lookup"><span data-stu-id="7097f-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="7097f-108">`ResourceGroupName`: standard resurs gruppen som anges av `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="7097f-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="7097f-109">`Location`: resurs gruppens plats</span><span class="sxs-lookup"><span data-stu-id="7097f-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="7097f-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="7097f-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="7097f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7097f-111">EXAMPLES</span></span>

### <span data-ttu-id="7097f-112">Skapa en signal tjänst</span><span class="sxs-lookup"><span data-stu-id="7097f-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="7097f-113">Ange ServiceMode och AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="7097f-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="7097f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7097f-114">PARAMETERS</span></span>

### <span data-ttu-id="7097f-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="7097f-115">-AllowedOrigin</span></span>
<span data-ttu-id="7097f-116">Tillåtna ursprung för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7097f-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="7097f-117">För att tillåta alla, Använd "\*" och ta bort alla andra ursprung från listan.</span><span class="sxs-lookup"><span data-stu-id="7097f-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="7097f-118">Snedstreck tillåts inte som en del av en domän eller efter TOPPnivå</span><span class="sxs-lookup"><span data-stu-id="7097f-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="7097f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7097f-119">-AsJob</span></span>
<span data-ttu-id="7097f-120">Kör cmdleten i bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="7097f-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="7097f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7097f-121">-DefaultProfile</span></span>
<span data-ttu-id="7097f-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7097f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7097f-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="7097f-123">-Location</span></span>
<span data-ttu-id="7097f-124">Signal tjänstens plats.</span><span class="sxs-lookup"><span data-stu-id="7097f-124">The SignalR service location.</span></span> <span data-ttu-id="7097f-125">Resurs gruppens plats kommer att användas om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="7097f-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="7097f-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="7097f-126">-Name</span></span>
<span data-ttu-id="7097f-127">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="7097f-127">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7097f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7097f-128">-ResourceGroupName</span></span>
<span data-ttu-id="7097f-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7097f-129">The resource group name.</span></span> <span data-ttu-id="7097f-130">Standard alternativet används om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="7097f-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="7097f-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="7097f-131">-ServiceMode</span></span>
<span data-ttu-id="7097f-132">Tjänst läget för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7097f-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="7097f-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="7097f-133">-Sku</span></span>
<span data-ttu-id="7097f-134">Tjänsten för avsändnings tjänster.</span><span class="sxs-lookup"><span data-stu-id="7097f-134">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7097f-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7097f-135">-Tag</span></span>
<span data-ttu-id="7097f-136">Taggarna för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="7097f-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="7097f-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="7097f-137">-UnitCount</span></span>
<span data-ttu-id="7097f-138">Signal tjänstens antal enheter, från 1 till 10.</span><span class="sxs-lookup"><span data-stu-id="7097f-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="7097f-139">Standardvärdet 1.</span><span class="sxs-lookup"><span data-stu-id="7097f-139">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7097f-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7097f-140">-Confirm</span></span>
<span data-ttu-id="7097f-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7097f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7097f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7097f-142">-WhatIf</span></span>
<span data-ttu-id="7097f-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7097f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7097f-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7097f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7097f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7097f-145">CommonParameters</span></span>
<span data-ttu-id="7097f-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7097f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7097f-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7097f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7097f-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7097f-148">INPUTS</span></span>

### <span data-ttu-id="7097f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7097f-149">System.String</span></span>

## <span data-ttu-id="7097f-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7097f-150">OUTPUTS</span></span>

### <span data-ttu-id="7097f-151">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="7097f-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="7097f-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7097f-152">NOTES</span></span>

## <span data-ttu-id="7097f-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7097f-153">RELATED LINKS</span></span>
