---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
ms.openlocfilehash: 4b4f3a416ece999641570a33101a3e7ab201ca3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577860"
---
# <span data-ttu-id="1ead8-101">New-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="1ead8-101">New-AzureRmSignalRKey</span></span>

## <span data-ttu-id="1ead8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ead8-102">SYNOPSIS</span></span>
<span data-ttu-id="1ead8-103">Återskapa en snabb tangenten för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="1ead8-103">Regenerate an access key for a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ead8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ead8-104">SYNTAX</span></span>

### <span data-ttu-id="1ead8-105">ResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1ead8-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ead8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ead8-106">ResourceIdParameterSet</span></span>
```
New-AzureRmSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ead8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ead8-107">InputObjectParameterSet</span></span>
```
New-AzureRmSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ead8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ead8-108">DESCRIPTION</span></span>
<span data-ttu-id="1ead8-109">Återskapa en snabb tangenten för en signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="1ead8-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="1ead8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ead8-110">EXAMPLES</span></span>

### <span data-ttu-id="1ead8-111">Återskapa primär nyckeln</span><span class="sxs-lookup"><span data-stu-id="1ead8-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="1ead8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ead8-112">PARAMETERS</span></span>

### <span data-ttu-id="1ead8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ead8-113">-DefaultProfile</span></span>
<span data-ttu-id="1ead8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ead8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ead8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ead8-115">-InputObject</span></span>
<span data-ttu-id="1ead8-116">Objektet Signalerare.</span><span class="sxs-lookup"><span data-stu-id="1ead8-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="1ead8-117">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="1ead8-117">-KeyType</span></span>
<span data-ttu-id="1ead8-118">Typ av primär eller sekundär.</span><span class="sxs-lookup"><span data-stu-id="1ead8-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="1ead8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ead8-119">-Name</span></span>
<span data-ttu-id="1ead8-120">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="1ead8-120">SignalR service name.</span></span>

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

### <span data-ttu-id="1ead8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ead8-121">-PassThru</span></span>
<span data-ttu-id="1ead8-122">Returnerar sant om genereringen lyckades.</span><span class="sxs-lookup"><span data-stu-id="1ead8-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="1ead8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ead8-123">-ResourceGroupName</span></span>
<span data-ttu-id="1ead8-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1ead8-124">Resource group name.</span></span>

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

### <span data-ttu-id="1ead8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ead8-125">-ResourceId</span></span>
<span data-ttu-id="1ead8-126">Avsändnings tjänstens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1ead8-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="1ead8-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ead8-127">-Confirm</span></span>
<span data-ttu-id="1ead8-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ead8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ead8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ead8-129">-WhatIf</span></span>
<span data-ttu-id="1ead8-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ead8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ead8-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ead8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ead8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ead8-132">CommonParameters</span></span>
<span data-ttu-id="1ead8-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ead8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ead8-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ead8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ead8-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ead8-135">INPUTS</span></span>

### <span data-ttu-id="1ead8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1ead8-136">System.String</span></span>
<span data-ttu-id="1ead8-137">Parametrar: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ead8-137">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="1ead8-138">Microsoft. Azure. commands. signaler. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="1ead8-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="1ead8-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ead8-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1ead8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ead8-140">OUTPUTS</span></span>

### <span data-ttu-id="1ead8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ead8-141">System.Boolean</span></span>

## <span data-ttu-id="1ead8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ead8-142">NOTES</span></span>

## <span data-ttu-id="1ead8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ead8-143">RELATED LINKS</span></span>
