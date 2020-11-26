---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269314"
---
# <span data-ttu-id="96419-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="96419-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="96419-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96419-102">SYNOPSIS</span></span>
<span data-ttu-id="96419-103">Tar bort en Azure-IpGroup.</span><span class="sxs-lookup"><span data-stu-id="96419-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="96419-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96419-104">SYNTAX</span></span>

### <span data-ttu-id="96419-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96419-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96419-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96419-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96419-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96419-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96419-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96419-108">DESCRIPTION</span></span>
<span data-ttu-id="96419-109">Cmdleten **Remove-AzIpGroup** tar bort en Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="96419-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="96419-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96419-110">EXAMPLES</span></span>

### <span data-ttu-id="96419-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="96419-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="96419-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="96419-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="96419-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="96419-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="96419-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96419-114">PARAMETERS</span></span>

### <span data-ttu-id="96419-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96419-115">-AsJob</span></span>
<span data-ttu-id="96419-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="96419-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96419-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96419-117">-DefaultProfile</span></span>
<span data-ttu-id="96419-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96419-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96419-119">-Force</span><span class="sxs-lookup"><span data-stu-id="96419-119">-Force</span></span>
<span data-ttu-id="96419-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="96419-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="96419-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="96419-121">-IpGroup</span></span>
<span data-ttu-id="96419-122">IpGroup.</span><span class="sxs-lookup"><span data-stu-id="96419-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96419-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="96419-123">-Name</span></span>
<span data-ttu-id="96419-124">Namnet på ipgroup.</span><span class="sxs-lookup"><span data-stu-id="96419-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96419-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96419-125">-PassThru</span></span>
<span data-ttu-id="96419-126">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="96419-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="96419-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96419-127">-ResourceGroupName</span></span>
<span data-ttu-id="96419-128">Resurs grupps namnet för ipgroup.</span><span class="sxs-lookup"><span data-stu-id="96419-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96419-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96419-129">-ResourceId</span></span>
<span data-ttu-id="96419-130">Resurs-ID för ipgroup.</span><span class="sxs-lookup"><span data-stu-id="96419-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96419-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96419-131">-Confirm</span></span>
<span data-ttu-id="96419-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96419-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96419-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96419-133">-WhatIf</span></span>
<span data-ttu-id="96419-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96419-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96419-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96419-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96419-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96419-136">CommonParameters</span></span>
<span data-ttu-id="96419-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96419-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96419-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96419-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96419-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96419-139">INPUTS</span></span>

### <span data-ttu-id="96419-140">System. String</span><span class="sxs-lookup"><span data-stu-id="96419-140">System.String</span></span>

### <span data-ttu-id="96419-141">Microsoft. Azure. commands. Networks. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="96419-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="96419-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96419-142">OUTPUTS</span></span>

### <span data-ttu-id="96419-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96419-143">System.Boolean</span></span>

## <span data-ttu-id="96419-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96419-144">NOTES</span></span>

## <span data-ttu-id="96419-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96419-145">RELATED LINKS</span></span>