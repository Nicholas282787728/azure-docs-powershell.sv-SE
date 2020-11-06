---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
ms.openlocfilehash: 5fcf62e592ed1e842c3dc6f4be21462170c4f83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577856"
---
# <span data-ttu-id="772c7-101">Remove-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="772c7-101">Remove-AzureRmSignalR</span></span>

## <span data-ttu-id="772c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="772c7-102">SYNOPSIS</span></span>
<span data-ttu-id="772c7-103">Ta bort en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="772c7-103">Remove a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="772c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="772c7-104">SYNTAX</span></span>

### <span data-ttu-id="772c7-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="772c7-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="772c7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="772c7-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="772c7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="772c7-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="772c7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="772c7-108">DESCRIPTION</span></span>
<span data-ttu-id="772c7-109">Ta bort en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="772c7-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="772c7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="772c7-110">EXAMPLES</span></span>

### <span data-ttu-id="772c7-111">Ta bort en signal tjänst</span><span class="sxs-lookup"><span data-stu-id="772c7-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="772c7-112">Ta bort all signal tjänst från en pipe</span><span class="sxs-lookup"><span data-stu-id="772c7-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup | Remove-AzureRmSignalR
```

## <span data-ttu-id="772c7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="772c7-113">PARAMETERS</span></span>

### <span data-ttu-id="772c7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="772c7-114">-AsJob</span></span>
<span data-ttu-id="772c7-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="772c7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="772c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772c7-116">-DefaultProfile</span></span>
<span data-ttu-id="772c7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="772c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="772c7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="772c7-118">-InputObject</span></span>
<span data-ttu-id="772c7-119">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="772c7-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="772c7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="772c7-120">-Name</span></span>
<span data-ttu-id="772c7-121">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="772c7-121">SignalR service name.</span></span>

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

### <span data-ttu-id="772c7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="772c7-122">-PassThru</span></span>
<span data-ttu-id="772c7-123">Returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="772c7-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="772c7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="772c7-124">-ResourceGroupName</span></span>
<span data-ttu-id="772c7-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="772c7-125">Resource group name.</span></span>

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

### <span data-ttu-id="772c7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="772c7-126">-ResourceId</span></span>
<span data-ttu-id="772c7-127">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="772c7-127">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="772c7-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="772c7-128">-Confirm</span></span>
<span data-ttu-id="772c7-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="772c7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="772c7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="772c7-130">-WhatIf</span></span>
<span data-ttu-id="772c7-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="772c7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="772c7-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="772c7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="772c7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772c7-133">CommonParameters</span></span>
<span data-ttu-id="772c7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="772c7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772c7-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="772c7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772c7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="772c7-136">INPUTS</span></span>

### <span data-ttu-id="772c7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="772c7-137">System.String</span></span>
<span data-ttu-id="772c7-138">Parametrar: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="772c7-138">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="772c7-139">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="772c7-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="772c7-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="772c7-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="772c7-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="772c7-141">OUTPUTS</span></span>

### <span data-ttu-id="772c7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="772c7-142">System.Boolean</span></span>

## <span data-ttu-id="772c7-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="772c7-143">NOTES</span></span>

## <span data-ttu-id="772c7-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="772c7-144">RELATED LINKS</span></span>
