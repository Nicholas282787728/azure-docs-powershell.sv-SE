---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259870"
---
# <span data-ttu-id="d5696-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="d5696-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="d5696-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5696-102">SYNOPSIS</span></span>
<span data-ttu-id="d5696-103">Återskapa en snabb tangenten för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="d5696-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="d5696-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5696-104">SYNTAX</span></span>

### <span data-ttu-id="d5696-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d5696-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5696-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5696-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5696-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5696-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5696-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5696-108">DESCRIPTION</span></span>
<span data-ttu-id="d5696-109">Återskapa en snabb tangenten för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="d5696-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="d5696-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5696-110">EXAMPLES</span></span>

### <span data-ttu-id="d5696-111">Återskapa primär nyckeln</span><span class="sxs-lookup"><span data-stu-id="d5696-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="d5696-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5696-112">PARAMETERS</span></span>

### <span data-ttu-id="d5696-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5696-113">-DefaultProfile</span></span>
<span data-ttu-id="d5696-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5696-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5696-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5696-115">-InputObject</span></span>
<span data-ttu-id="d5696-116">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="d5696-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d5696-117">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="d5696-117">-KeyType</span></span>
<span data-ttu-id="d5696-118">Typ av primär eller sekundär.</span><span class="sxs-lookup"><span data-stu-id="d5696-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5696-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d5696-119">-Name</span></span>
<span data-ttu-id="d5696-120">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="d5696-120">SignalR service name.</span></span>

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

### <span data-ttu-id="d5696-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5696-121">-PassThru</span></span>
<span data-ttu-id="d5696-122">Returnerar sant om genereringen lyckades.</span><span class="sxs-lookup"><span data-stu-id="d5696-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="d5696-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5696-123">-ResourceGroupName</span></span>
<span data-ttu-id="d5696-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d5696-124">Resource group name.</span></span>

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

### <span data-ttu-id="d5696-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5696-125">-ResourceId</span></span>
<span data-ttu-id="d5696-126">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d5696-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d5696-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d5696-127">-Confirm</span></span>
<span data-ttu-id="d5696-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d5696-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5696-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5696-129">-WhatIf</span></span>
<span data-ttu-id="d5696-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d5696-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5696-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d5696-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5696-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5696-132">CommonParameters</span></span>
<span data-ttu-id="d5696-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5696-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5696-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5696-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5696-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5696-135">INPUTS</span></span>

### <span data-ttu-id="d5696-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d5696-136">System.String</span></span>
### <span data-ttu-id="d5696-137">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d5696-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="d5696-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5696-138">OUTPUTS</span></span>

### <span data-ttu-id="d5696-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5696-139">System.Boolean</span></span>
## <span data-ttu-id="d5696-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5696-140">NOTES</span></span>

## <span data-ttu-id="d5696-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5696-141">RELATED LINKS</span></span>