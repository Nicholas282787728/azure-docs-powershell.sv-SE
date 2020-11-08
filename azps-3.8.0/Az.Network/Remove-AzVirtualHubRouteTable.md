---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091712"
---
# <span data-ttu-id="e4972-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4972-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="e4972-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4972-102">SYNOPSIS</span></span>
<span data-ttu-id="e4972-103">Ta bort en tabell resurs för virtuell hubb som är associerad med ett virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="e4972-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="e4972-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4972-104">SYNTAX</span></span>

### <span data-ttu-id="e4972-105">ByVirtualHubRouteTableName (standard)</span><span class="sxs-lookup"><span data-stu-id="e4972-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4972-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e4972-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4972-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="e4972-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4972-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="e4972-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4972-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4972-109">DESCRIPTION</span></span>
<span data-ttu-id="e4972-110">Tar bort den angivna routningstabellen som är kopplad till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="e4972-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="e4972-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4972-111">EXAMPLES</span></span>

### <span data-ttu-id="e4972-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e4972-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="e4972-113">Det här kommandot tar bort routeTable1 för den virtuella nav westushub.</span><span class="sxs-lookup"><span data-stu-id="e4972-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="e4972-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4972-114">PARAMETERS</span></span>

### <span data-ttu-id="e4972-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4972-115">-AsJob</span></span>
<span data-ttu-id="e4972-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e4972-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4972-117">-DefaultProfile</span></span>
<span data-ttu-id="e4972-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4972-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e4972-119">-Force</span></span>
<span data-ttu-id="e4972-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="e4972-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="e4972-121">-HubName</span></span>
<span data-ttu-id="e4972-122">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="e4972-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4972-123">-InputObject</span></span>
<span data-ttu-id="e4972-124">Virtualhubroutetable-resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e4972-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4972-125">-Name</span></span>
<span data-ttu-id="e4972-126">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e4972-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4972-127">-PassThru</span></span>
<span data-ttu-id="e4972-128">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="e4972-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4972-129">-ResourceGroupName</span></span>
<span data-ttu-id="e4972-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e4972-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4972-131">-ResourceId</span></span>
<span data-ttu-id="e4972-132">Resurs-ID för den virtualhubroutetable-resurs som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e4972-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="e4972-133">-VirtualHub</span></span>
<span data-ttu-id="e4972-134">{{Fill VirtualHub Description}}</span><span class="sxs-lookup"><span data-stu-id="e4972-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4972-135">-Confirm</span></span>
<span data-ttu-id="e4972-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4972-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4972-137">-WhatIf</span></span>
<span data-ttu-id="e4972-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e4972-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4972-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e4972-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4972-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4972-140">CommonParameters</span></span>
<span data-ttu-id="e4972-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4972-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4972-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4972-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4972-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4972-143">INPUTS</span></span>

### <span data-ttu-id="e4972-144">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e4972-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="e4972-145">Microsoft. Azure. commands. Networks. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e4972-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="e4972-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e4972-146">System.String</span></span>

## <span data-ttu-id="e4972-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4972-147">OUTPUTS</span></span>

### <span data-ttu-id="e4972-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4972-148">System.Boolean</span></span>

## <span data-ttu-id="e4972-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4972-149">NOTES</span></span>

## <span data-ttu-id="e4972-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4972-150">RELATED LINKS</span></span>