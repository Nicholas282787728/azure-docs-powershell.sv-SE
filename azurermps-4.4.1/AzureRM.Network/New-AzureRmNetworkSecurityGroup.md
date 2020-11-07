---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: f2d9781f205df70e5becbc53f597f27791ca6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755932"
---
# <span data-ttu-id="2267d-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2267d-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="2267d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2267d-102">SYNOPSIS</span></span>
<span data-ttu-id="2267d-103">Skapar en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="2267d-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2267d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2267d-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2267d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2267d-105">DESCRIPTION</span></span>
<span data-ttu-id="2267d-106">Cmdleten **New-AzureRmNetworkSecurityGroup** skapar en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="2267d-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="2267d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2267d-107">EXAMPLES</span></span>

### <span data-ttu-id="2267d-108">1: skapa en ny nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="2267d-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="2267d-109">Det här kommandot skapar en ny Azure nätverks säkerhets grupp med namnet "nsg1" i resurs gruppen "RG1" i plats "västkusten".</span><span class="sxs-lookup"><span data-stu-id="2267d-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="2267d-110">2: skapa en detaljerad nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="2267d-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="2267d-111">Steg: 1 Skapa en säkerhets regel som tillåter åtkomst från Internet till port 3389.</span><span class="sxs-lookup"><span data-stu-id="2267d-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="2267d-112">Steg: 2 Skapa en säkerhets regel som tillåter åtkomst från Internet till port 80.</span><span class="sxs-lookup"><span data-stu-id="2267d-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="2267d-113">Steg: 3 Lägg till reglerna ovan till en ny NSG som heter NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="2267d-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="2267d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2267d-114">PARAMETERS</span></span>

### <span data-ttu-id="2267d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2267d-115">-Force</span></span>
<span data-ttu-id="2267d-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2267d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2267d-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="2267d-117">-Location</span></span>
<span data-ttu-id="2267d-118">Anger den region som du vill skapa en nätverks säkerhets grupp för.</span><span class="sxs-lookup"><span data-stu-id="2267d-118">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="2267d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2267d-119">-Name</span></span>
<span data-ttu-id="2267d-120">Anger namnet på nätverks säkerhets gruppen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2267d-120">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="2267d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2267d-121">-ResourceGroupName</span></span>
<span data-ttu-id="2267d-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2267d-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2267d-123">Denna cmdlet skapar en nätverks säkerhets grupp i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2267d-123">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2267d-124">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="2267d-124">-SecurityRules</span></span>
<span data-ttu-id="2267d-125">Anger en lista över nätverks säkerhets regel objekt som ska skapas i en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="2267d-125">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2267d-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2267d-126">-Tag</span></span>
<span data-ttu-id="2267d-127">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="2267d-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2267d-128">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="2267d-128">For example:</span></span>

<span data-ttu-id="2267d-129">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="2267d-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2267d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2267d-130">-Confirm</span></span>
<span data-ttu-id="2267d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2267d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2267d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2267d-132">-WhatIf</span></span>
<span data-ttu-id="2267d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2267d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2267d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2267d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2267d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2267d-135">-DefaultProfile</span></span>
<span data-ttu-id="2267d-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2267d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2267d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2267d-137">CommonParameters</span></span>
<span data-ttu-id="2267d-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2267d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2267d-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2267d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2267d-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2267d-140">INPUTS</span></span>

## <span data-ttu-id="2267d-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2267d-141">OUTPUTS</span></span>

### <span data-ttu-id="2267d-142">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2267d-142">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="2267d-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2267d-143">NOTES</span></span>

## <span data-ttu-id="2267d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2267d-144">RELATED LINKS</span></span>

[<span data-ttu-id="2267d-145">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2267d-145">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="2267d-146">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2267d-146">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="2267d-147">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2267d-147">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
