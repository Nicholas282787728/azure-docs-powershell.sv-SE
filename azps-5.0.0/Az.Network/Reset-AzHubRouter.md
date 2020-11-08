---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272048"
---
# <span data-ttu-id="c181e-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="c181e-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="c181e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c181e-102">SYNOPSIS</span></span>
<span data-ttu-id="c181e-103">Återställer RoutingState för en VirtualHub-resurs.</span><span class="sxs-lookup"><span data-stu-id="c181e-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="c181e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c181e-104">SYNTAX</span></span>

### <span data-ttu-id="c181e-105">ByVirtualHubName (standard)</span><span class="sxs-lookup"><span data-stu-id="c181e-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c181e-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c181e-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c181e-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="c181e-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c181e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c181e-108">DESCRIPTION</span></span>
<span data-ttu-id="c181e-109">Återställer statusen för en befintlig VirtualHub-resurs endast om Dirigerings statusen för det virtuella navet inte har etablerats.</span><span class="sxs-lookup"><span data-stu-id="c181e-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="c181e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c181e-110">EXAMPLES</span></span>

### <span data-ttu-id="c181e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c181e-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="c181e-112">Återställ statusen för en virtuell hubb med dess ResourceGroupName och ResourceName.</span><span class="sxs-lookup"><span data-stu-id="c181e-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="c181e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c181e-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="c181e-114">Återställ statusen för den virtuella hubben till dess ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c181e-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="c181e-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c181e-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="c181e-116">Återställ statusen för den virtuella hubben för det virtuellt navet med ett indatavärde.</span><span class="sxs-lookup"><span data-stu-id="c181e-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="c181e-117">Indatavärdet är av typen PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="c181e-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="c181e-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="c181e-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="c181e-119">Ett befintligt virtuellt nav-objekt kan hämtas och sedan skickas som indatafil-AzHubRouter.</span><span class="sxs-lookup"><span data-stu-id="c181e-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="c181e-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c181e-120">PARAMETERS</span></span>

### <span data-ttu-id="c181e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c181e-121">-AsJob</span></span>
<span data-ttu-id="c181e-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c181e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c181e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c181e-123">-DefaultProfile</span></span>
<span data-ttu-id="c181e-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c181e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c181e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c181e-125">-Force</span></span>
<span data-ttu-id="c181e-126">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="c181e-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c181e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c181e-127">-InputObject</span></span>
<span data-ttu-id="c181e-128">Det virtuella nav-objekt som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="c181e-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c181e-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="c181e-129">-Name</span></span>
<span data-ttu-id="c181e-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c181e-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c181e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c181e-131">-ResourceGroupName</span></span>
<span data-ttu-id="c181e-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c181e-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c181e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c181e-133">-ResourceId</span></span>
<span data-ttu-id="c181e-134">Resurs-ID för det virtuella nav som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="c181e-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c181e-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c181e-135">-Confirm</span></span>
<span data-ttu-id="c181e-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c181e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c181e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c181e-137">-WhatIf</span></span>
<span data-ttu-id="c181e-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c181e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c181e-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c181e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c181e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c181e-140">CommonParameters</span></span>
<span data-ttu-id="c181e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c181e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c181e-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c181e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c181e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c181e-143">INPUTS</span></span>

### <span data-ttu-id="c181e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c181e-144">System.String</span></span>

### <span data-ttu-id="c181e-145">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c181e-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="c181e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c181e-146">OUTPUTS</span></span>

### <span data-ttu-id="c181e-147">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c181e-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="c181e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c181e-148">NOTES</span></span>

## <span data-ttu-id="c181e-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c181e-149">RELATED LINKS</span></span>

[<span data-ttu-id="c181e-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c181e-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
