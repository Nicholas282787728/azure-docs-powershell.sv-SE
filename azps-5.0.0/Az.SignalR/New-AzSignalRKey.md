---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272605"
---
# <span data-ttu-id="705bf-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="705bf-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="705bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="705bf-102">SYNOPSIS</span></span>
<span data-ttu-id="705bf-103">Återskapa en snabb tangenten för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="705bf-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="705bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="705bf-104">SYNTAX</span></span>

### <span data-ttu-id="705bf-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="705bf-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="705bf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="705bf-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="705bf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="705bf-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="705bf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="705bf-108">DESCRIPTION</span></span>
<span data-ttu-id="705bf-109">Återskapa en snabb tangenten för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="705bf-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="705bf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="705bf-110">EXAMPLES</span></span>

### <span data-ttu-id="705bf-111">Återskapa primär nyckeln</span><span class="sxs-lookup"><span data-stu-id="705bf-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="705bf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="705bf-112">PARAMETERS</span></span>

### <span data-ttu-id="705bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="705bf-113">-DefaultProfile</span></span>
<span data-ttu-id="705bf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="705bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="705bf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="705bf-115">-InputObject</span></span>
<span data-ttu-id="705bf-116">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="705bf-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="705bf-117">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="705bf-117">-KeyType</span></span>
<span data-ttu-id="705bf-118">Typ av primär eller sekundär.</span><span class="sxs-lookup"><span data-stu-id="705bf-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="705bf-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="705bf-119">-Name</span></span>
<span data-ttu-id="705bf-120">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="705bf-120">SignalR service name.</span></span>

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

### <span data-ttu-id="705bf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="705bf-121">-PassThru</span></span>
<span data-ttu-id="705bf-122">Returnerar sant om genereringen lyckades.</span><span class="sxs-lookup"><span data-stu-id="705bf-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="705bf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="705bf-123">-ResourceGroupName</span></span>
<span data-ttu-id="705bf-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="705bf-124">Resource group name.</span></span>

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

### <span data-ttu-id="705bf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="705bf-125">-ResourceId</span></span>
<span data-ttu-id="705bf-126">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="705bf-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="705bf-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="705bf-127">-Confirm</span></span>
<span data-ttu-id="705bf-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="705bf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="705bf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="705bf-129">-WhatIf</span></span>
<span data-ttu-id="705bf-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="705bf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="705bf-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="705bf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="705bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705bf-132">CommonParameters</span></span>
<span data-ttu-id="705bf-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="705bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705bf-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="705bf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705bf-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="705bf-135">INPUTS</span></span>

### <span data-ttu-id="705bf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="705bf-136">System.String</span></span>
### <span data-ttu-id="705bf-137">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="705bf-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="705bf-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="705bf-138">OUTPUTS</span></span>

### <span data-ttu-id="705bf-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="705bf-139">System.Boolean</span></span>
## <span data-ttu-id="705bf-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="705bf-140">NOTES</span></span>

## <span data-ttu-id="705bf-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="705bf-141">RELATED LINKS</span></span>
