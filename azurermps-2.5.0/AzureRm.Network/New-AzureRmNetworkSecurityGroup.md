---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 3603adcce2ce39cc4e0a2dd57869a6ca10c48998
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930181"
---
# <span data-ttu-id="6e5d7-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e5d7-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="6e5d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="6e5d7-103">Skapar en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e5d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e5d7-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e5d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e5d7-105">DESCRIPTION</span></span>
<span data-ttu-id="6e5d7-106">Cmdleten **New-AzureRmNetworkSecurityGroup** skapar en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="6e5d7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e5d7-107">EXAMPLES</span></span>

### <span data-ttu-id="6e5d7-108">1: skapa en ny nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="6e5d7-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="6e5d7-109">Det här kommandot skapar en ny Azure nätverks säkerhets grupp med namnet "nsg1" i resurs gruppen "RG1" i plats "västkusten".</span><span class="sxs-lookup"><span data-stu-id="6e5d7-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="6e5d7-110">2: skapa en detaljerad nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="6e5d7-110">2: Create a detailed network security group</span></span>
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

<span data-ttu-id="6e5d7-111">Steg: 1 Skapa en säkerhets regel som tillåter åtkomst från Internet till port 3389.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="6e5d7-112">Steg: 2 Skapa en säkerhets regel som tillåter åtkomst från Internet till port 80.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="6e5d7-113">Steg: 3 Lägg till reglerna ovan till en ny NSG som heter NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="6e5d7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e5d7-114">PARAMETERS</span></span>

### <span data-ttu-id="6e5d7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e5d7-115">-AsJob</span></span>
<span data-ttu-id="6e5d7-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6e5d7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e5d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e5d7-117">-DefaultProfile</span></span>
<span data-ttu-id="6e5d7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e5d7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6e5d7-119">-Force</span></span>
<span data-ttu-id="6e5d7-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e5d7-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="6e5d7-121">-Location</span></span>
<span data-ttu-id="6e5d7-122">Anger den region som du vill skapa en nätverks säkerhets grupp för.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="6e5d7-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6e5d7-123">-Name</span></span>
<span data-ttu-id="6e5d7-124">Anger namnet på nätverks säkerhets gruppen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="6e5d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e5d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="6e5d7-126">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6e5d7-127">Denna cmdlet skapar en nätverks säkerhets grupp i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6e5d7-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="6e5d7-128">-SecurityRules</span></span>
<span data-ttu-id="6e5d7-129">Anger en lista över nätverks säkerhets regel objekt som ska skapas i en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="6e5d7-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6e5d7-130">-Tag</span></span>
<span data-ttu-id="6e5d7-131">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6e5d7-132">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="6e5d7-132">For example:</span></span>

<span data-ttu-id="6e5d7-133">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="6e5d7-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e5d7-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6e5d7-134">-Confirm</span></span>
<span data-ttu-id="6e5d7-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e5d7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e5d7-136">-WhatIf</span></span>
<span data-ttu-id="6e5d7-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e5d7-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e5d7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e5d7-139">CommonParameters</span></span>
<span data-ttu-id="6e5d7-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e5d7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e5d7-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e5d7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e5d7-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e5d7-142">INPUTS</span></span>

## <span data-ttu-id="6e5d7-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e5d7-143">OUTPUTS</span></span>

### <span data-ttu-id="6e5d7-144">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e5d7-144">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="6e5d7-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e5d7-145">NOTES</span></span>

## <span data-ttu-id="6e5d7-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e5d7-146">RELATED LINKS</span></span>

[<span data-ttu-id="6e5d7-147">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e5d7-147">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="6e5d7-148">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e5d7-148">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="6e5d7-149">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6e5d7-149">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
