---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 7665170d5ca71e73e787dbe22e84f3372497c687
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748030"
---
# <span data-ttu-id="86e7a-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86e7a-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="86e7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="86e7a-103">Skapar en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="86e7a-103">Creates a network security group.</span></span>

## <span data-ttu-id="86e7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86e7a-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e7a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="86e7a-106">Cmdleten **New-AzNetworkSecurityGroup** skapar en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="86e7a-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="86e7a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86e7a-107">EXAMPLES</span></span>

### <span data-ttu-id="86e7a-108">1: skapa en ny nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="86e7a-108">1: Create a new network security group</span></span>
```
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="86e7a-109">Det här kommandot skapar en ny Azure nätverks säkerhets grupp med namnet "nsg1" i resurs gruppen "RG1" i plats "västkusten".</span><span class="sxs-lookup"><span data-stu-id="86e7a-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="86e7a-110">2: skapa en detaljerad nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="86e7a-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="86e7a-111">Steg: 1 Skapa en säkerhets regel som tillåter åtkomst från Internet till port 3389.</span><span class="sxs-lookup"><span data-stu-id="86e7a-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="86e7a-112">Steg: 2 Skapa en säkerhets regel som tillåter åtkomst från Internet till port 80.</span><span class="sxs-lookup"><span data-stu-id="86e7a-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="86e7a-113">Steg: 3 Lägg till reglerna ovan till en ny NSG som heter NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="86e7a-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="86e7a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86e7a-114">PARAMETERS</span></span>

### <span data-ttu-id="86e7a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86e7a-115">-AsJob</span></span>
<span data-ttu-id="86e7a-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="86e7a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86e7a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e7a-117">-DefaultProfile</span></span>
<span data-ttu-id="86e7a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86e7a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86e7a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="86e7a-119">-Force</span></span>
<span data-ttu-id="86e7a-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="86e7a-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="86e7a-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="86e7a-121">-Location</span></span>
<span data-ttu-id="86e7a-122">Anger den region som du vill skapa en nätverks säkerhets grupp för.</span><span class="sxs-lookup"><span data-stu-id="86e7a-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="86e7a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="86e7a-123">-Name</span></span>
<span data-ttu-id="86e7a-124">Anger namnet på nätverks säkerhets gruppen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="86e7a-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="86e7a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e7a-125">-ResourceGroupName</span></span>
<span data-ttu-id="86e7a-126">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="86e7a-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="86e7a-127">Denna cmdlet skapar en nätverks säkerhets grupp i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="86e7a-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="86e7a-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="86e7a-128">-SecurityRules</span></span>
<span data-ttu-id="86e7a-129">Anger en lista över nätverks säkerhets regel objekt som ska skapas i en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="86e7a-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86e7a-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="86e7a-130">-Tag</span></span>
<span data-ttu-id="86e7a-131">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="86e7a-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="86e7a-132">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="86e7a-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86e7a-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86e7a-133">-Confirm</span></span>
<span data-ttu-id="86e7a-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86e7a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86e7a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e7a-135">-WhatIf</span></span>
<span data-ttu-id="86e7a-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86e7a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86e7a-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86e7a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86e7a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e7a-138">CommonParameters</span></span>
<span data-ttu-id="86e7a-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e7a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e7a-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86e7a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e7a-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86e7a-141">INPUTS</span></span>

### <span data-ttu-id="86e7a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="86e7a-142">System.String</span></span>

### <span data-ttu-id="86e7a-143">Microsoft. Azure. commands. Network. Models. PSSecurityRule []</span><span class="sxs-lookup"><span data-stu-id="86e7a-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="86e7a-144">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="86e7a-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="86e7a-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86e7a-145">OUTPUTS</span></span>

### <span data-ttu-id="86e7a-146">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86e7a-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="86e7a-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86e7a-147">NOTES</span></span>

## <span data-ttu-id="86e7a-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86e7a-148">RELATED LINKS</span></span>

[<span data-ttu-id="86e7a-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86e7a-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="86e7a-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86e7a-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="86e7a-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="86e7a-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
