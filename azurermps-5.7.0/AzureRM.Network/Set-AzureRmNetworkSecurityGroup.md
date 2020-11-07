---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: ab009608100bc4cbb4915f6bc3e82d44d9e08cd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757398"
---
# <span data-ttu-id="f309a-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f309a-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="f309a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f309a-102">SYNOPSIS</span></span>
<span data-ttu-id="f309a-103">Anger mål tillståndet för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="f309a-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f309a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f309a-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f309a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f309a-105">DESCRIPTION</span></span>
<span data-ttu-id="f309a-106">Cmdleten **set-AzureRmNetworkSecurityGroup** anger mål tillståndet för en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="f309a-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="f309a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f309a-107">EXAMPLES</span></span>

### <span data-ttu-id="f309a-108">Exempel 1: Ange mål tillstånd för en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="f309a-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="f309a-109">Det här kommandot hämtar Azure nätverks säkerhets gruppen med namnet Nsg1 och lägger till en nätverks säkerhets regel med namnet Rdp-Rule för att tillåta Internet trafik på port 3389 till det hämtade objektet nätverks säkerhets grupp med hjälp av Add-AzureRmNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f309a-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="f309a-110">Kommandot behåller den ändrade Azure Network Security-gruppen med **set-AzureRmNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="f309a-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="f309a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f309a-111">PARAMETERS</span></span>

### <span data-ttu-id="f309a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f309a-112">-AsJob</span></span>
<span data-ttu-id="f309a-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f309a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f309a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f309a-114">-DefaultProfile</span></span>
<span data-ttu-id="f309a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f309a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f309a-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f309a-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f309a-117">Ett nätverks säkerhets grupp objekt som representerar mål tillståndet där cmdleten ställer in nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="f309a-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="f309a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f309a-118">CommonParameters</span></span>
<span data-ttu-id="f309a-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f309a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f309a-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f309a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f309a-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f309a-121">INPUTS</span></span>

### <span data-ttu-id="f309a-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f309a-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="f309a-123">Parametern ' NetworkSecurityGroup ' godkänner värdet av typen ' PSNetworkSecurityGroup ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f309a-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="f309a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f309a-124">OUTPUTS</span></span>

### <span data-ttu-id="f309a-125">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f309a-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="f309a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f309a-126">NOTES</span></span>

## <span data-ttu-id="f309a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f309a-127">RELATED LINKS</span></span>

[<span data-ttu-id="f309a-128">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f309a-128">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="f309a-129">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f309a-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="f309a-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f309a-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


