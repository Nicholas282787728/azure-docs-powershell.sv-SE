---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 51e84639808859a74d2070eff3a9cab984deb21c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919009"
---
# <span data-ttu-id="184bd-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="184bd-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="184bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="184bd-102">SYNOPSIS</span></span>
<span data-ttu-id="184bd-103">Ta bort NAT gateway-resurs.</span><span class="sxs-lookup"><span data-stu-id="184bd-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="184bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="184bd-104">SYNTAX</span></span>

### <span data-ttu-id="184bd-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="184bd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184bd-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="184bd-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="184bd-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="184bd-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="184bd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="184bd-108">DESCRIPTION</span></span>
<span data-ttu-id="184bd-109">Ta bort NAT-gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="184bd-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="184bd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="184bd-110">EXAMPLES</span></span>

### <span data-ttu-id="184bd-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="184bd-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="184bd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="184bd-112">PARAMETERS</span></span>

### <span data-ttu-id="184bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="184bd-113">-AsJob</span></span>
<span data-ttu-id="184bd-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="184bd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="184bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184bd-115">-DefaultProfile</span></span>
<span data-ttu-id="184bd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="184bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="184bd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="184bd-117">-Force</span></span>
<span data-ttu-id="184bd-118">Fråga inte efter bekräftelse om du vill ta bort resursen.</span><span class="sxs-lookup"><span data-stu-id="184bd-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="184bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="184bd-119">-InputObject</span></span>
<span data-ttu-id="184bd-120">Anger NAT-gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="184bd-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="184bd-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="184bd-121">-Name</span></span>
<span data-ttu-id="184bd-122">Namn på NAT-gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="184bd-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184bd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="184bd-123">-PassThru</span></span>
<span data-ttu-id="184bd-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="184bd-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="184bd-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="184bd-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="184bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="184bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="184bd-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="184bd-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="184bd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="184bd-128">-ResourceId</span></span>
<span data-ttu-id="184bd-129">Resurs-ID som är kopplat till NAT-gatewayen.</span><span class="sxs-lookup"><span data-stu-id="184bd-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184bd-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="184bd-130">-Confirm</span></span>
<span data-ttu-id="184bd-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="184bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="184bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="184bd-132">-WhatIf</span></span>
<span data-ttu-id="184bd-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="184bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="184bd-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="184bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="184bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184bd-135">CommonParameters</span></span>
<span data-ttu-id="184bd-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="184bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184bd-137">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="184bd-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184bd-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="184bd-138">INPUTS</span></span>

### <span data-ttu-id="184bd-139">Microsoft. Azure. commands. Networks. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="184bd-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="184bd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="184bd-140">System.String</span></span>

## <span data-ttu-id="184bd-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="184bd-141">OUTPUTS</span></span>

### <span data-ttu-id="184bd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="184bd-142">System.Boolean</span></span>

## <span data-ttu-id="184bd-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="184bd-143">NOTES</span></span>

## <span data-ttu-id="184bd-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="184bd-144">RELATED LINKS</span></span>
