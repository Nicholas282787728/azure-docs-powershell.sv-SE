---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270758"
---
# <span data-ttu-id="2a436-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="2a436-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="2a436-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a436-102">SYNOPSIS</span></span>
<span data-ttu-id="2a436-103">Ta bort en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="2a436-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="2a436-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a436-104">SYNTAX</span></span>

### <span data-ttu-id="2a436-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2a436-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a436-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a436-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a436-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a436-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a436-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a436-108">DESCRIPTION</span></span>
<span data-ttu-id="2a436-109">Ta bort en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="2a436-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="2a436-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a436-110">EXAMPLES</span></span>

### <span data-ttu-id="2a436-111">Ta bort en signal tjänst</span><span class="sxs-lookup"><span data-stu-id="2a436-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="2a436-112">Ta bort all signal tjänst från en pipe</span><span class="sxs-lookup"><span data-stu-id="2a436-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="2a436-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a436-113">PARAMETERS</span></span>

### <span data-ttu-id="2a436-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a436-114">-AsJob</span></span>
<span data-ttu-id="2a436-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2a436-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a436-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a436-116">-DefaultProfile</span></span>
<span data-ttu-id="2a436-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a436-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a436-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a436-118">-InputObject</span></span>
<span data-ttu-id="2a436-119">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="2a436-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="2a436-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a436-120">-Name</span></span>
<span data-ttu-id="2a436-121">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="2a436-121">SignalR service name.</span></span>

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

### <span data-ttu-id="2a436-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a436-122">-PassThru</span></span>
<span data-ttu-id="2a436-123">Returnerar sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="2a436-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a436-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a436-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a436-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2a436-125">Resource group name.</span></span>

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

### <span data-ttu-id="2a436-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a436-126">-ResourceId</span></span>
<span data-ttu-id="2a436-127">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2a436-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="2a436-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a436-128">-Confirm</span></span>
<span data-ttu-id="2a436-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a436-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a436-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a436-130">-WhatIf</span></span>
<span data-ttu-id="2a436-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a436-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a436-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a436-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a436-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a436-133">CommonParameters</span></span>
<span data-ttu-id="2a436-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a436-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a436-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a436-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a436-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a436-136">INPUTS</span></span>

### <span data-ttu-id="2a436-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2a436-137">System.String</span></span>
### <span data-ttu-id="2a436-138">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="2a436-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="2a436-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a436-139">OUTPUTS</span></span>

### <span data-ttu-id="2a436-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a436-140">System.Boolean</span></span>
## <span data-ttu-id="2a436-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a436-141">NOTES</span></span>

## <span data-ttu-id="2a436-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a436-142">RELATED LINKS</span></span>
