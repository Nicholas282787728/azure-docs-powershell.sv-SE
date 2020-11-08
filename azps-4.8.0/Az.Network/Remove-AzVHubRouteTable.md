---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262075"
---
# <span data-ttu-id="468b9-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b9-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="468b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="468b9-102">SYNOPSIS</span></span>
<span data-ttu-id="468b9-103">Ta bort en tabell resurs för en hubb som är associerad med en VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="468b9-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="468b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="468b9-104">SYNTAX</span></span>

### <span data-ttu-id="468b9-105">ByVHubRouteTableName (standard)</span><span class="sxs-lookup"><span data-stu-id="468b9-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="468b9-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="468b9-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="468b9-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="468b9-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="468b9-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="468b9-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="468b9-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="468b9-109">DESCRIPTION</span></span>
<span data-ttu-id="468b9-110">Tar bort den angivna Hub-routningstabellen som är kopplad till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="468b9-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="468b9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="468b9-111">EXAMPLES</span></span>

### <span data-ttu-id="468b9-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="468b9-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="468b9-113">Det här kommandot tar bort nav-routningstabellen för det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="468b9-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="468b9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="468b9-114">PARAMETERS</span></span>

### <span data-ttu-id="468b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="468b9-115">-AsJob</span></span>
<span data-ttu-id="468b9-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="468b9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="468b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468b9-117">-DefaultProfile</span></span>
<span data-ttu-id="468b9-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="468b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="468b9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="468b9-119">-Force</span></span>
<span data-ttu-id="468b9-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="468b9-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="468b9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="468b9-121">-InputObject</span></span>
<span data-ttu-id="468b9-122">Vhubroutetable-resursen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="468b9-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="468b9-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="468b9-123">-Name</span></span>
<span data-ttu-id="468b9-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="468b9-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="468b9-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="468b9-125">-ParentObject</span></span>
<span data-ttu-id="468b9-126">Överordnat objekt för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="468b9-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="468b9-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="468b9-127">-ParentResourceName</span></span>
<span data-ttu-id="468b9-128">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="468b9-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="468b9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="468b9-129">-PassThru</span></span>
<span data-ttu-id="468b9-130">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="468b9-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="468b9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468b9-131">-ResourceGroupName</span></span>
<span data-ttu-id="468b9-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="468b9-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="468b9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="468b9-133">-ResourceId</span></span>
<span data-ttu-id="468b9-134">Resurs-ID för den vhubroutetable-resurs som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="468b9-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="468b9-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="468b9-135">-Confirm</span></span>
<span data-ttu-id="468b9-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="468b9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="468b9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="468b9-137">-WhatIf</span></span>
<span data-ttu-id="468b9-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="468b9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="468b9-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="468b9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="468b9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468b9-140">CommonParameters</span></span>
<span data-ttu-id="468b9-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="468b9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468b9-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="468b9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468b9-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="468b9-143">INPUTS</span></span>

### <span data-ttu-id="468b9-144">Microsoft. Azure. commands. Networks. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="468b9-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="468b9-145">Microsoft. Azure. commands. Networks. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b9-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="468b9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="468b9-146">System.String</span></span>

## <span data-ttu-id="468b9-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="468b9-147">OUTPUTS</span></span>

### <span data-ttu-id="468b9-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="468b9-148">System.Boolean</span></span>

## <span data-ttu-id="468b9-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="468b9-149">NOTES</span></span>

## <span data-ttu-id="468b9-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="468b9-150">RELATED LINKS</span></span>

[<span data-ttu-id="468b9-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b9-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="468b9-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="468b9-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="468b9-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b9-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="468b9-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="468b9-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)