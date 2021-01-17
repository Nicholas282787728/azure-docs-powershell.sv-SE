---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401000"
---
# <span data-ttu-id="41c39-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="41c39-101">New-AzNatGateway</span></span>

## <span data-ttu-id="41c39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41c39-102">SYNOPSIS</span></span>
<span data-ttu-id="41c39-103">Skapa en ny NAT-gatewayenhet med egenskaper offentlig IP-adress/offentlig IP-prefix, IdleTimeoutInMinutes och SKU.</span><span class="sxs-lookup"><span data-stu-id="41c39-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="41c39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41c39-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41c39-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41c39-105">DESCRIPTION</span></span>
<span data-ttu-id="41c39-106">Cmdleten **New-AzNatGateway** skapar en NAT gateway-resurs.</span><span class="sxs-lookup"><span data-stu-id="41c39-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="41c39-107">En natgateway kräver följande:</span><span class="sxs-lookup"><span data-stu-id="41c39-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="41c39-108">Offentlig IP-adress och/eller offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="41c39-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="41c39-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="41c39-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="41c39-110">N</span><span class="sxs-lookup"><span data-stu-id="41c39-110">Sku</span></span>
- <span data-ttu-id="41c39-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c39-111">ResourceGroupName</span></span>
- <span data-ttu-id="41c39-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="41c39-112">ResourceName</span></span>
- <span data-ttu-id="41c39-113">Plats</span><span class="sxs-lookup"><span data-stu-id="41c39-113">Location</span></span>

## <span data-ttu-id="41c39-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41c39-114">EXAMPLES</span></span>

### <span data-ttu-id="41c39-115">Exempel 1: skapa NAT-gateway med offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="41c39-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="41c39-116">Exempel 2: skapa NAT-gateway med offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="41c39-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="41c39-117">Exempel 3: skapa NAT-gateway med offentlig IP-adress i tillgänglighets zon 1</span><span class="sxs-lookup"><span data-stu-id="41c39-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="41c39-118">Första kommandot skapar standard offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="41c39-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="41c39-119">Det andra kommandot skapar NAT-gateway med offentlig IP-adress i tillgänglighets zon 1.</span><span class="sxs-lookup"><span data-stu-id="41c39-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="41c39-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41c39-120">PARAMETERS</span></span>

### <span data-ttu-id="41c39-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41c39-121">-AsJob</span></span>
<span data-ttu-id="41c39-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="41c39-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41c39-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c39-123">-DefaultProfile</span></span>
<span data-ttu-id="41c39-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41c39-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c39-125">-Force</span><span class="sxs-lookup"><span data-stu-id="41c39-125">-Force</span></span>
<span data-ttu-id="41c39-126">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="41c39-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="41c39-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="41c39-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="41c39-128">Inaktive tids timeout för NAT-gatewayen.</span><span class="sxs-lookup"><span data-stu-id="41c39-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="41c39-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="41c39-129">-Location</span></span>
<span data-ttu-id="41c39-130">Platsen.</span><span class="sxs-lookup"><span data-stu-id="41c39-130">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c39-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="41c39-131">-Name</span></span>
<span data-ttu-id="41c39-132">Namnet på NAT-gatewayen.</span><span class="sxs-lookup"><span data-stu-id="41c39-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c39-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="41c39-133">-PublicIpAddress</span></span>
<span data-ttu-id="41c39-134">En matris med offentliga IP-adresser som är kopplade till NAT gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="41c39-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="41c39-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="41c39-135">-PublicIpPrefix</span></span>
<span data-ttu-id="41c39-136">En matris med offentliga IP-prefix som är kopplade till NAT gateway-resursen.</span><span class="sxs-lookup"><span data-stu-id="41c39-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="41c39-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c39-137">-ResourceGroupName</span></span>
<span data-ttu-id="41c39-138">Namnet på den som heter NAT.</span><span class="sxs-lookup"><span data-stu-id="41c39-138">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c39-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="41c39-139">-Sku</span></span>
<span data-ttu-id="41c39-140">Namn på en NAT-gateway-SKU.</span><span class="sxs-lookup"><span data-stu-id="41c39-140">Name of a NAT gateway SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c39-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="41c39-141">-Tag</span></span>
<span data-ttu-id="41c39-142">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="41c39-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c39-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="41c39-143">-Zone</span></span>
<span data-ttu-id="41c39-144">En lista över tillgänglighets zoner som betecknar den zon där NAT-gateway ska distribueras.</span><span class="sxs-lookup"><span data-stu-id="41c39-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c39-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41c39-145">-Confirm</span></span>
<span data-ttu-id="41c39-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41c39-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c39-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c39-147">-WhatIf</span></span>
<span data-ttu-id="41c39-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41c39-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c39-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41c39-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c39-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c39-150">CommonParameters</span></span>
<span data-ttu-id="41c39-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c39-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c39-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41c39-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c39-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41c39-153">INPUTS</span></span>

### <span data-ttu-id="41c39-154">System. String</span><span class="sxs-lookup"><span data-stu-id="41c39-154">System.String</span></span>

### <span data-ttu-id="41c39-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="41c39-155">System.Int32</span></span>

### <span data-ttu-id="41c39-156">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="41c39-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="41c39-157">Microsoft. Azure. commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="41c39-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="41c39-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41c39-158">OUTPUTS</span></span>

### <span data-ttu-id="41c39-159">Microsoft. Azure. commands. Networks. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="41c39-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="41c39-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41c39-160">NOTES</span></span>

## <span data-ttu-id="41c39-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41c39-161">RELATED LINKS</span></span>
