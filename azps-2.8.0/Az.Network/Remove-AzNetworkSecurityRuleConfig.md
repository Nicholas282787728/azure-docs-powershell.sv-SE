---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 24cdadc4e7dcbfc138bd6e3dc126d2d65ee56435
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918053"
---
# <span data-ttu-id="ad4b7-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4b7-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="ad4b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4b7-103">Tar bort en nätverks säkerhets regel från en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="ad4b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad4b7-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad4b7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad4b7-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4b7-106">Cmdleten **Remove-AzNetworkSecurityRuleConfig** tar bort en nätverks säkerhets regel från en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="ad4b7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad4b7-107">EXAMPLES</span></span>

### <span data-ttu-id="ad4b7-108">Exempel 1: ta bort en nätverks säkerhets regel konfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4b7-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="ad4b7-109">Det första kommandot skapar en nätverks säkerhets regel som heter RDP-Rule och lagrar den sedan i $rule 1-variabeln.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="ad4b7-110">Det andra kommandot skapar en nätverks säkerhets grupp med regeln i $rule 1 och lagrar sedan nätverks säkerhets gruppen i $nsg variabel.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="ad4b7-111">Det tredje kommandot tar bort nätverks säkerhets regel konfigurationen med namnet RDP-regel från nätverks säkerhets gruppen i $nsg.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="ad4b7-112">Med kommandot tillbaka sparas ändringen.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-112">The forth command saves the change.</span></span>

## <span data-ttu-id="ad4b7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad4b7-113">PARAMETERS</span></span>

### <span data-ttu-id="ad4b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4b7-114">-DefaultProfile</span></span>
<span data-ttu-id="ad4b7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad4b7-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad4b7-116">-Name</span></span>
<span data-ttu-id="ad4b7-117">Anger namnet på den nätverks säkerhets regel som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad4b7-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ad4b7-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ad4b7-119">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="ad4b7-120">Det här objektet innehåller nätverks säkerhets regel konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-120">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4b7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4b7-121">CommonParameters</span></span>
<span data-ttu-id="ad4b7-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4b7-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4b7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4b7-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad4b7-124">INPUTS</span></span>

### <span data-ttu-id="ad4b7-125">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ad4b7-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ad4b7-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad4b7-126">OUTPUTS</span></span>

### <span data-ttu-id="ad4b7-127">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ad4b7-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ad4b7-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad4b7-128">NOTES</span></span>

## <span data-ttu-id="ad4b7-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad4b7-129">RELATED LINKS</span></span>

[<span data-ttu-id="ad4b7-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4b7-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ad4b7-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4b7-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ad4b7-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ad4b7-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="ad4b7-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4b7-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ad4b7-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad4b7-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


