---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 1602c9e5fb0244239eea4eec53661c3392ac0354
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922040"
---
# <span data-ttu-id="2ec87-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ec87-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="2ec87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ec87-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec87-103">Tar bort en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="2ec87-103">Removes a load balancer.</span></span>

## <span data-ttu-id="2ec87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ec87-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec87-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ec87-105">DESCRIPTION</span></span>
<span data-ttu-id="2ec87-106">Cmdleten **Remove-AzLoadBalancer** tar bort en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="2ec87-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="2ec87-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ec87-107">EXAMPLES</span></span>

### <span data-ttu-id="2ec87-108">Exempel 1: ta bort en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="2ec87-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2ec87-109">Det här kommandot tar bort belastningsutjämnaren med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2ec87-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2ec87-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ec87-110">PARAMETERS</span></span>

### <span data-ttu-id="2ec87-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ec87-111">-AsJob</span></span>
<span data-ttu-id="2ec87-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2ec87-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ec87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec87-113">-DefaultProfile</span></span>
<span data-ttu-id="2ec87-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec87-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2ec87-115">-Force</span></span>
<span data-ttu-id="2ec87-116">Anger att belastningsutjämnaren tar bort belastnings utjämning oavsett om det är tilldelade resurser eller inte.</span><span class="sxs-lookup"><span data-stu-id="2ec87-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ec87-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ec87-117">-Name</span></span>
<span data-ttu-id="2ec87-118">Anger namnet på belastningsutjämnaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2ec87-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ec87-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ec87-119">-PassThru</span></span>
<span data-ttu-id="2ec87-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2ec87-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2ec87-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2ec87-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ec87-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec87-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ec87-123">Anger namnet på den resurs grupp som innehåller belastningsutjämnaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2ec87-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ec87-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ec87-124">-Confirm</span></span>
<span data-ttu-id="2ec87-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ec87-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec87-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec87-126">-WhatIf</span></span>
<span data-ttu-id="2ec87-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ec87-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ec87-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ec87-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec87-129">CommonParameters</span></span>
<span data-ttu-id="2ec87-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec87-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec87-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec87-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ec87-132">INPUTS</span></span>

## <span data-ttu-id="2ec87-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ec87-133">OUTPUTS</span></span>

## <span data-ttu-id="2ec87-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ec87-134">NOTES</span></span>

## <span data-ttu-id="2ec87-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ec87-135">RELATED LINKS</span></span>

[<span data-ttu-id="2ec87-136">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ec87-136">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2ec87-137">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ec87-137">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="2ec87-138">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ec87-138">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


