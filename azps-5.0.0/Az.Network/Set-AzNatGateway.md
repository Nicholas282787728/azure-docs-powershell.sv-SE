---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270467"
---
# <span data-ttu-id="94b86-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="94b86-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="94b86-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94b86-102">SYNOPSIS</span></span>
<span data-ttu-id="94b86-103">Uppdatera NAT gateway-resursen med offentlig IP-adress, offentlig IP-prefix och IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="94b86-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="94b86-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94b86-104">SYNTAX</span></span>

### <span data-ttu-id="94b86-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="94b86-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94b86-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94b86-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94b86-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94b86-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94b86-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94b86-108">DESCRIPTION</span></span>
<span data-ttu-id="94b86-109">Uppdatera NAT gateway-resursen med offentlig IP-adress, offentlig IP-prefix och IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="94b86-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="94b86-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94b86-110">EXAMPLES</span></span>

### <span data-ttu-id="94b86-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="94b86-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="94b86-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94b86-112">PARAMETERS</span></span>

### <span data-ttu-id="94b86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94b86-113">-AsJob</span></span>
<span data-ttu-id="94b86-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="94b86-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94b86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b86-115">-DefaultProfile</span></span>
<span data-ttu-id="94b86-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94b86-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94b86-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="94b86-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="94b86-118">Inaktive tids timeout för NAT-gatewayen.</span><span class="sxs-lookup"><span data-stu-id="94b86-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94b86-119">-InputObject</span></span>
<span data-ttu-id="94b86-120">Anger NAT-gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="94b86-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="94b86-121">-Name</span></span>
<span data-ttu-id="94b86-122">Namn på NAT-gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="94b86-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="94b86-123">-PublicIpAddress</span></span>
<span data-ttu-id="94b86-124">En matris med offentliga IP-adresser som är kopplade till NAT gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="94b86-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="94b86-125">-PublicIpPrefix</span></span>
<span data-ttu-id="94b86-126">En matris med offentliga IP-prefix som är kopplade till NAT gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="94b86-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b86-127">-ResourceGroupName</span></span>
<span data-ttu-id="94b86-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="94b86-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94b86-129">-ResourceId</span></span>
<span data-ttu-id="94b86-130">Anger ID för NAT-gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="94b86-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94b86-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94b86-131">-Confirm</span></span>
<span data-ttu-id="94b86-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94b86-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94b86-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b86-133">-WhatIf</span></span>
<span data-ttu-id="94b86-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94b86-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94b86-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94b86-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94b86-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b86-136">CommonParameters</span></span>
<span data-ttu-id="94b86-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b86-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b86-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94b86-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b86-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94b86-139">INPUTS</span></span>

### <span data-ttu-id="94b86-140">System. String</span><span class="sxs-lookup"><span data-stu-id="94b86-140">System.String</span></span>

### <span data-ttu-id="94b86-141">Microsoft. Azure. commands. Networks. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="94b86-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="94b86-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94b86-142">OUTPUTS</span></span>

### <span data-ttu-id="94b86-143">Microsoft. Azure. commands. Networks. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="94b86-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="94b86-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94b86-144">NOTES</span></span>

## <span data-ttu-id="94b86-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94b86-145">RELATED LINKS</span></span>
