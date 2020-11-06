---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
ms.openlocfilehash: d5b7e5480ea3078dadf5280b4f683280dcd00ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577864"
---
# <span data-ttu-id="a22f4-101">New-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="a22f4-101">New-AzureRmSignalR</span></span>

## <span data-ttu-id="a22f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a22f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a22f4-103">Skapa en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="a22f4-103">Create a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a22f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a22f4-104">SYNTAX</span></span>

```
New-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a22f4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a22f4-105">DESCRIPTION</span></span>
<span data-ttu-id="a22f4-106">Skapa en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="a22f4-106">Create a SignalR service.</span></span>
<span data-ttu-id="a22f4-107">Följande värden används för parametrar om de inte anges:</span><span class="sxs-lookup"><span data-stu-id="a22f4-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="a22f4-108">`ResourceGroupName`: standard resurs gruppen som anges av `Set-AzureRmDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="a22f4-108">`ResourceGroupName`: the default resource group set by `Set-AzureRmDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="a22f4-109">`Location`: resurs gruppens plats</span><span class="sxs-lookup"><span data-stu-id="a22f4-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="a22f4-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="a22f4-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="a22f4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a22f4-111">EXAMPLES</span></span>

### <span data-ttu-id="a22f4-112">Skapa en serivce</span><span class="sxs-lookup"><span data-stu-id="a22f4-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzureRmSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="a22f4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a22f4-113">PARAMETERS</span></span>

### <span data-ttu-id="a22f4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a22f4-114">-AsJob</span></span>
<span data-ttu-id="a22f4-115">Kör cmdleten i bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="a22f4-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="a22f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a22f4-116">-DefaultProfile</span></span>
<span data-ttu-id="a22f4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a22f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a22f4-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="a22f4-118">-Location</span></span>
<span data-ttu-id="a22f4-119">Signal tjänstens plats.</span><span class="sxs-lookup"><span data-stu-id="a22f4-119">The SignalR service location.</span></span> <span data-ttu-id="a22f4-120">Resurs gruppens plats kommer att användas om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="a22f4-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="a22f4-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a22f4-121">-Name</span></span>
<span data-ttu-id="a22f4-122">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="a22f4-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="a22f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a22f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="a22f4-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a22f4-124">The resource group name.</span></span> <span data-ttu-id="a22f4-125">Standard alternativet används om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="a22f4-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="a22f4-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="a22f4-126">-Sku</span></span>
<span data-ttu-id="a22f4-127">Tjänsten för avsändnings tjänster.</span><span class="sxs-lookup"><span data-stu-id="a22f4-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="a22f4-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a22f4-128">-Tag</span></span>
<span data-ttu-id="a22f4-129">Taggarna för signal tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a22f4-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="a22f4-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="a22f4-130">-UnitCount</span></span>
<span data-ttu-id="a22f4-131">Signal tjänstens antal enheter, från 1 till 10.</span><span class="sxs-lookup"><span data-stu-id="a22f4-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="a22f4-132">Standardvärdet 1.</span><span class="sxs-lookup"><span data-stu-id="a22f4-132">Default to 1.</span></span>

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

### <span data-ttu-id="a22f4-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a22f4-133">-Confirm</span></span>
<span data-ttu-id="a22f4-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a22f4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a22f4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a22f4-135">-WhatIf</span></span>
<span data-ttu-id="a22f4-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a22f4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a22f4-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a22f4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a22f4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22f4-138">CommonParameters</span></span>
<span data-ttu-id="a22f4-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a22f4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22f4-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a22f4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22f4-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a22f4-141">INPUTS</span></span>

### <span data-ttu-id="a22f4-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="a22f4-142">None</span></span>

## <span data-ttu-id="a22f4-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a22f4-143">OUTPUTS</span></span>

### <span data-ttu-id="a22f4-144">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="a22f4-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="a22f4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a22f4-145">NOTES</span></span>

## <span data-ttu-id="a22f4-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a22f4-146">RELATED LINKS</span></span>
