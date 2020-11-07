---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 96f6acdda93de63486f117c99572b4680fb025e6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928702"
---
# <span data-ttu-id="269e6-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="269e6-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="269e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="269e6-102">SYNOPSIS</span></span>
<span data-ttu-id="269e6-103">Tar bort en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="269e6-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="269e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="269e6-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="269e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="269e6-105">DESCRIPTION</span></span>
<span data-ttu-id="269e6-106">Cmdleten **Remove-AzureRmLoadBalancer** tar bort en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="269e6-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="269e6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="269e6-107">EXAMPLES</span></span>

### <span data-ttu-id="269e6-108">Exempel 1: ta bort en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="269e6-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="269e6-109">Det här kommandot tar bort belastningsutjämnaren med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="269e6-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="269e6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="269e6-110">PARAMETERS</span></span>

### <span data-ttu-id="269e6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="269e6-111">-AsJob</span></span>
<span data-ttu-id="269e6-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="269e6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="269e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="269e6-113">-DefaultProfile</span></span>
<span data-ttu-id="269e6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="269e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="269e6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="269e6-115">-Force</span></span>
<span data-ttu-id="269e6-116">Anger att belastningsutjämnaren tar bort belastnings utjämning oavsett om det är tilldelade resurser eller inte.</span><span class="sxs-lookup"><span data-stu-id="269e6-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="269e6-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="269e6-117">-Name</span></span>
<span data-ttu-id="269e6-118">Anger namnet på belastningsutjämnaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="269e6-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="269e6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="269e6-119">-PassThru</span></span>
<span data-ttu-id="269e6-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="269e6-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="269e6-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="269e6-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="269e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="269e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="269e6-123">Anger namnet på den resurs grupp som innehåller belastningsutjämnaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="269e6-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="269e6-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="269e6-124">-Confirm</span></span>
<span data-ttu-id="269e6-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="269e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="269e6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="269e6-126">-WhatIf</span></span>
<span data-ttu-id="269e6-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="269e6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="269e6-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="269e6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="269e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="269e6-129">CommonParameters</span></span>
<span data-ttu-id="269e6-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="269e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="269e6-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="269e6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="269e6-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="269e6-132">INPUTS</span></span>

## <span data-ttu-id="269e6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="269e6-133">OUTPUTS</span></span>

## <span data-ttu-id="269e6-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="269e6-134">NOTES</span></span>

## <span data-ttu-id="269e6-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="269e6-135">RELATED LINKS</span></span>

[<span data-ttu-id="269e6-136">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="269e6-136">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="269e6-137">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="269e6-137">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="269e6-138">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="269e6-138">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


