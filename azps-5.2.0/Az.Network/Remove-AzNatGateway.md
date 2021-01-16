---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393451"
---
# <span data-ttu-id="5a5e7-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5a5e7-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="5a5e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="5a5e7-103">Ta bort NAT gateway-resurs.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="5a5e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a5e7-104">SYNTAX</span></span>

### <span data-ttu-id="5a5e7-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5a5e7-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a5e7-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a5e7-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a5e7-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a5e7-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a5e7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a5e7-108">DESCRIPTION</span></span>
<span data-ttu-id="5a5e7-109">Ta bort NAT-gateway-resurs</span><span class="sxs-lookup"><span data-stu-id="5a5e7-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="5a5e7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a5e7-110">EXAMPLES</span></span>

### <span data-ttu-id="5a5e7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5a5e7-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="5a5e7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a5e7-112">PARAMETERS</span></span>

### <span data-ttu-id="5a5e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a5e7-113">-AsJob</span></span>
<span data-ttu-id="5a5e7-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5a5e7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a5e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a5e7-115">-DefaultProfile</span></span>
<span data-ttu-id="5a5e7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a5e7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5a5e7-117">-Force</span></span>
<span data-ttu-id="5a5e7-118">Fråga inte efter bekräftelse om du vill ta bort resursen.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="5a5e7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a5e7-119">-InputObject</span></span>
<span data-ttu-id="5a5e7-120">Anger NAT-gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="5a5e7-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a5e7-121">-Name</span></span>
<span data-ttu-id="5a5e7-122">Namn på NAT-gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="5a5e7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a5e7-123">-PassThru</span></span>
<span data-ttu-id="5a5e7-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5a5e7-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5a5e7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a5e7-126">-ResourceGroupName</span></span>
<span data-ttu-id="5a5e7-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="5a5e7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a5e7-128">-ResourceId</span></span>
<span data-ttu-id="5a5e7-129">Resurs-ID som är kopplat till NAT-gatewayen.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="5a5e7-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a5e7-130">-Confirm</span></span>
<span data-ttu-id="5a5e7-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a5e7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a5e7-132">-WhatIf</span></span>
<span data-ttu-id="5a5e7-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a5e7-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a5e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a5e7-135">CommonParameters</span></span>
<span data-ttu-id="5a5e7-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a5e7-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a5e7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a5e7-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a5e7-138">INPUTS</span></span>

### <span data-ttu-id="5a5e7-139">Microsoft. Azure. commands. Networks. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="5a5e7-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="5a5e7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5a5e7-140">System.String</span></span>

## <span data-ttu-id="5a5e7-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a5e7-141">OUTPUTS</span></span>

### <span data-ttu-id="5a5e7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a5e7-142">System.Boolean</span></span>

## <span data-ttu-id="5a5e7-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a5e7-143">NOTES</span></span>

## <span data-ttu-id="5a5e7-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a5e7-144">RELATED LINKS</span></span>
