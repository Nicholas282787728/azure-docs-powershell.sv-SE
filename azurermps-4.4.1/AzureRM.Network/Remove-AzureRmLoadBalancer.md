---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 6757c9c0b9eeb0b3408a07713c62812d361d814a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585404"
---
# <span data-ttu-id="c50c0-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50c0-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="c50c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c50c0-102">SYNOPSIS</span></span>
<span data-ttu-id="c50c0-103">Tar bort en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c50c0-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c50c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c50c0-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c50c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c50c0-105">DESCRIPTION</span></span>
<span data-ttu-id="c50c0-106">Cmdleten **Remove-AzureRmLoadBalancer** tar bort en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c50c0-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="c50c0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c50c0-107">EXAMPLES</span></span>

### <span data-ttu-id="c50c0-108">Exempel 1: ta bort en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="c50c0-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c50c0-109">Det här kommandot tar bort belastningsutjämnaren med namnet MyLoadBalancer i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c50c0-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="c50c0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c50c0-110">PARAMETERS</span></span>

### <span data-ttu-id="c50c0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c50c0-111">-Force</span></span>
<span data-ttu-id="c50c0-112">Anger att belastningsutjämnaren tar bort belastnings utjämning oavsett om det är tilldelade resurser eller inte.</span><span class="sxs-lookup"><span data-stu-id="c50c0-112">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c50c0-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c50c0-113">-Name</span></span>
<span data-ttu-id="c50c0-114">Anger namnet på belastningsutjämnaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c50c0-114">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="c50c0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c50c0-115">-PassThru</span></span>
<span data-ttu-id="c50c0-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c50c0-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c50c0-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c50c0-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c50c0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c50c0-118">-ResourceGroupName</span></span>
<span data-ttu-id="c50c0-119">Anger namnet på den resurs grupp som innehåller belastningsutjämnaren som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c50c0-119">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="c50c0-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c50c0-120">-Confirm</span></span>
<span data-ttu-id="c50c0-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c50c0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c50c0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c50c0-122">-WhatIf</span></span>
<span data-ttu-id="c50c0-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c50c0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c50c0-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c50c0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c50c0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c50c0-125">-DefaultProfile</span></span>
<span data-ttu-id="c50c0-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c50c0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c50c0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c50c0-127">CommonParameters</span></span>
<span data-ttu-id="c50c0-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c50c0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c50c0-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c50c0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c50c0-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c50c0-130">INPUTS</span></span>

## <span data-ttu-id="c50c0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c50c0-131">OUTPUTS</span></span>

## <span data-ttu-id="c50c0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c50c0-132">NOTES</span></span>

## <span data-ttu-id="c50c0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c50c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="c50c0-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50c0-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c50c0-135">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50c0-135">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="c50c0-136">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c50c0-136">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


