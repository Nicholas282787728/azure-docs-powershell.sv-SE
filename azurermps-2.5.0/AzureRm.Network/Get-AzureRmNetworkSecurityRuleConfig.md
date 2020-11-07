---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 55f2ad108b6392a2f17c7b1539c5ebe7cccc3c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931282"
---
# <span data-ttu-id="1efd1-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1efd1-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="1efd1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1efd1-102">SYNOPSIS</span></span>
<span data-ttu-id="1efd1-103">Få en nätverks säkerhets regel konfiguration för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="1efd1-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1efd1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1efd1-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1efd1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1efd1-105">DESCRIPTION</span></span>
<span data-ttu-id="1efd1-106">Cmdleten **Get-AzureRmNetworkSecurityRuleConfig** hämtar en nätverks säkerhets regel för en Azure nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="1efd1-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="1efd1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1efd1-107">EXAMPLES</span></span>

### <span data-ttu-id="1efd1-108">1: hämtar en nätverks säkerhets regel konfiguration</span><span class="sxs-lookup"><span data-stu-id="1efd1-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="1efd1-109">Det här kommandot hämtar standard regeln med namnet "AllowInternetOutBound" från Azure Network Security Group med namnet "nsg1" i resurs gruppen "RG1"</span><span class="sxs-lookup"><span data-stu-id="1efd1-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="1efd1-110">2: Hämta en nätverks säkerhets regel konfiguration med endast namnet</span><span class="sxs-lookup"><span data-stu-id="1efd1-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="1efd1-111">Det här kommandot hämtar den användardefinierade regeln med "RDP-Rule" från Azure Network Security Group med namnet "nsg1" i resurs gruppen "RG1"</span><span class="sxs-lookup"><span data-stu-id="1efd1-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="1efd1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1efd1-112">PARAMETERS</span></span>

### <span data-ttu-id="1efd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1efd1-113">-DefaultProfile</span></span>
<span data-ttu-id="1efd1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1efd1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1efd1-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="1efd1-115">-DefaultRules</span></span>
<span data-ttu-id="1efd1-116">Anger om den här cmdleten hämtar en användardefinierad regel konfiguration eller en standard regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1efd1-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="1efd1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1efd1-117">-Name</span></span>
<span data-ttu-id="1efd1-118">Anger namnet på nätverks säkerhets regelns konfiguration som ska visas.</span><span class="sxs-lookup"><span data-stu-id="1efd1-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="1efd1-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1efd1-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1efd1-120">Anger ett **NetworkSecurityGroup** -objekt som innehåller nätverks säkerhets regel konfigurationen för att få.</span><span class="sxs-lookup"><span data-stu-id="1efd1-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="1efd1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1efd1-121">CommonParameters</span></span>
<span data-ttu-id="1efd1-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1efd1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1efd1-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1efd1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1efd1-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1efd1-124">INPUTS</span></span>

### <span data-ttu-id="1efd1-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1efd1-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="1efd1-126">Parametern ' NetworkSecurityGroup ' godkänner värdet av typen ' PSNetworkSecurityGroup ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="1efd1-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="1efd1-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1efd1-127">OUTPUTS</span></span>

### <span data-ttu-id="1efd1-128">Microsoft. Azure. commands. Networks. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="1efd1-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="1efd1-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1efd1-129">NOTES</span></span>

## <span data-ttu-id="1efd1-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1efd1-130">RELATED LINKS</span></span>

[<span data-ttu-id="1efd1-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1efd1-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1efd1-132">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1efd1-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1efd1-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1efd1-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="1efd1-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1efd1-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


