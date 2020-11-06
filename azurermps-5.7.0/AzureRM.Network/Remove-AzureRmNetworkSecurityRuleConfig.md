---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: fa75146ef26fc19108b918211a83289f73bfe4cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574250"
---
# <span data-ttu-id="94141-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94141-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="94141-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94141-102">SYNOPSIS</span></span>
<span data-ttu-id="94141-103">Tar bort en nätverks säkerhets regel från en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="94141-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94141-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94141-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94141-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94141-105">DESCRIPTION</span></span>
<span data-ttu-id="94141-106">Cmdleten **Remove-AzureRmNetworkSecurityRuleConfig** tar bort en nätverks säkerhets regel från en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="94141-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="94141-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94141-107">EXAMPLES</span></span>

### <span data-ttu-id="94141-108">Exempel 1: ta bort en nätverks säkerhets regel konfiguration</span><span class="sxs-lookup"><span data-stu-id="94141-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="94141-109">Det första kommandot skapar en nätverks säkerhets regel som heter RDP-Rule och lagrar den sedan i $rule 1-variabeln.</span><span class="sxs-lookup"><span data-stu-id="94141-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="94141-110">Det andra kommandot skapar en nätverks säkerhets grupp med regeln i $rule 1 och lagrar sedan nätverks säkerhets gruppen i $nsg variabel.</span><span class="sxs-lookup"><span data-stu-id="94141-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="94141-111">Det tredje kommandot tar bort nätverks säkerhets regel konfigurationen med namnet RDP-regel från nätverks säkerhets gruppen i $nsg.</span><span class="sxs-lookup"><span data-stu-id="94141-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="94141-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94141-112">PARAMETERS</span></span>

### <span data-ttu-id="94141-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94141-113">-DefaultProfile</span></span>
<span data-ttu-id="94141-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94141-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94141-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="94141-115">-Name</span></span>
<span data-ttu-id="94141-116">Anger namnet på den nätverks säkerhets regel som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="94141-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94141-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="94141-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="94141-118">Anger ett **NetworkSecurityGroup** -objekt.</span><span class="sxs-lookup"><span data-stu-id="94141-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="94141-119">Det här objektet innehåller nätverks säkerhets regel konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="94141-119">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94141-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94141-120">CommonParameters</span></span>
<span data-ttu-id="94141-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94141-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94141-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94141-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94141-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94141-123">INPUTS</span></span>

### <span data-ttu-id="94141-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="94141-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="94141-125">Parametern ' NetworkSecurityGroup ' godkänner värdet av typen ' PSNetworkSecurityGroup ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="94141-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="94141-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94141-126">OUTPUTS</span></span>

### <span data-ttu-id="94141-127">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="94141-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="94141-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94141-128">NOTES</span></span>

## <span data-ttu-id="94141-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94141-129">RELATED LINKS</span></span>

[<span data-ttu-id="94141-130">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94141-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="94141-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94141-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="94141-132">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="94141-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="94141-133">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94141-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="94141-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94141-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


