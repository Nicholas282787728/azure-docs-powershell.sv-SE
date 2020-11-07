---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: b91a807d5499236d45e84a9a064e7f64daa1fb57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918070"
---
# <span data-ttu-id="53a73-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53a73-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="53a73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53a73-102">SYNOPSIS</span></span>
<span data-ttu-id="53a73-103">Tar bort en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="53a73-103">Removes a load balancer.</span></span>

## <span data-ttu-id="53a73-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53a73-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53a73-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53a73-105">DESCRIPTION</span></span>
<span data-ttu-id="53a73-106">Cmdleten **Remove-AzLoadBalancer** tar bort en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="53a73-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="53a73-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53a73-107">EXAMPLES</span></span>

### <span data-ttu-id="53a73-108">Exempel 1: ta bort en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="53a73-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="53a73-109">Det här kommandot tar bort belastningsutjämnaren med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="53a73-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="53a73-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53a73-110">PARAMETERS</span></span>

### <span data-ttu-id="53a73-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53a73-111">-AsJob</span></span>
<span data-ttu-id="53a73-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="53a73-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53a73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a73-113">-DefaultProfile</span></span>
<span data-ttu-id="53a73-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53a73-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a73-115">-Force</span><span class="sxs-lookup"><span data-stu-id="53a73-115">-Force</span></span>
<span data-ttu-id="53a73-116">Anger att belastningsutjämnaren tar bort belastnings utjämning oavsett om det är tilldelade resurser eller inte.</span><span class="sxs-lookup"><span data-stu-id="53a73-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="53a73-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="53a73-117">-Name</span></span>
<span data-ttu-id="53a73-118">Anger namnet på belastningsutjämnaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="53a73-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a73-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53a73-119">-PassThru</span></span>
<span data-ttu-id="53a73-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="53a73-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="53a73-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="53a73-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="53a73-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a73-122">-ResourceGroupName</span></span>
<span data-ttu-id="53a73-123">Anger namnet på den resurs grupp som innehåller belastningsutjämnaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="53a73-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a73-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53a73-124">-Confirm</span></span>
<span data-ttu-id="53a73-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53a73-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a73-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a73-126">-WhatIf</span></span>
<span data-ttu-id="53a73-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53a73-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a73-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53a73-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a73-129">CommonParameters</span></span>
<span data-ttu-id="53a73-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a73-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53a73-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a73-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53a73-132">INPUTS</span></span>

### <span data-ttu-id="53a73-133">System. String</span><span class="sxs-lookup"><span data-stu-id="53a73-133">System.String</span></span>

## <span data-ttu-id="53a73-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53a73-134">OUTPUTS</span></span>

### <span data-ttu-id="53a73-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53a73-135">System.Boolean</span></span>

## <span data-ttu-id="53a73-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53a73-136">NOTES</span></span>

## <span data-ttu-id="53a73-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53a73-137">RELATED LINKS</span></span>

[<span data-ttu-id="53a73-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53a73-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="53a73-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53a73-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="53a73-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="53a73-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


