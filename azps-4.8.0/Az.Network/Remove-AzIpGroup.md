---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258212"
---
# <span data-ttu-id="40d72-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="40d72-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="40d72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40d72-102">SYNOPSIS</span></span>
<span data-ttu-id="40d72-103">Tar bort en Azure-IpGroup.</span><span class="sxs-lookup"><span data-stu-id="40d72-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="40d72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40d72-104">SYNTAX</span></span>

### <span data-ttu-id="40d72-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d72-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d72-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d72-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d72-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d72-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d72-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40d72-108">DESCRIPTION</span></span>
<span data-ttu-id="40d72-109">Cmdleten **Remove-AzIpGroup** tar bort en Azure-IpGroup</span><span class="sxs-lookup"><span data-stu-id="40d72-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="40d72-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40d72-110">EXAMPLES</span></span>

### <span data-ttu-id="40d72-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40d72-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="40d72-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="40d72-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="40d72-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="40d72-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="40d72-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40d72-114">PARAMETERS</span></span>

### <span data-ttu-id="40d72-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40d72-115">-AsJob</span></span>
<span data-ttu-id="40d72-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="40d72-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40d72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d72-117">-DefaultProfile</span></span>
<span data-ttu-id="40d72-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40d72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d72-119">-Force</span><span class="sxs-lookup"><span data-stu-id="40d72-119">-Force</span></span>
<span data-ttu-id="40d72-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="40d72-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="40d72-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="40d72-121">-IpGroup</span></span>
<span data-ttu-id="40d72-122">IpGroup.</span><span class="sxs-lookup"><span data-stu-id="40d72-122">The ipGroup input object.</span></span>

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

### <span data-ttu-id="40d72-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="40d72-123">-Name</span></span>
<span data-ttu-id="40d72-124">Namnet på ipgroup.</span><span class="sxs-lookup"><span data-stu-id="40d72-124">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="40d72-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40d72-125">-PassThru</span></span>
<span data-ttu-id="40d72-126">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="40d72-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="40d72-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d72-127">-ResourceGroupName</span></span>
<span data-ttu-id="40d72-128">Resurs grupps namnet för ipgroup.</span><span class="sxs-lookup"><span data-stu-id="40d72-128">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="40d72-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40d72-129">-ResourceId</span></span>
<span data-ttu-id="40d72-130">Resurs-ID för ipgroup.</span><span class="sxs-lookup"><span data-stu-id="40d72-130">The ipgroup resource Id.</span></span>

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

### <span data-ttu-id="40d72-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40d72-131">-Confirm</span></span>
<span data-ttu-id="40d72-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40d72-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d72-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d72-133">-WhatIf</span></span>
<span data-ttu-id="40d72-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40d72-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d72-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40d72-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d72-136">CommonParameters</span></span>
<span data-ttu-id="40d72-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d72-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40d72-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d72-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40d72-139">INPUTS</span></span>

### <span data-ttu-id="40d72-140">System. String</span><span class="sxs-lookup"><span data-stu-id="40d72-140">System.String</span></span>

### <span data-ttu-id="40d72-141">Microsoft. Azure. commands. Networks. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="40d72-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="40d72-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40d72-142">OUTPUTS</span></span>

### <span data-ttu-id="40d72-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40d72-143">System.Boolean</span></span>

## <span data-ttu-id="40d72-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40d72-144">NOTES</span></span>

## <span data-ttu-id="40d72-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40d72-145">RELATED LINKS</span></span>
