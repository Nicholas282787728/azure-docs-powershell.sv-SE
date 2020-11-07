---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924193"
---
# <span data-ttu-id="7aca2-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7aca2-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="7aca2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7aca2-102">SYNOPSIS</span></span>
<span data-ttu-id="7aca2-103">Anger mål tillståndet för en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="7aca2-103">Sets the goal state for a network security group.</span></span>

## <span data-ttu-id="7aca2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7aca2-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aca2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7aca2-105">DESCRIPTION</span></span>
<span data-ttu-id="7aca2-106">Cmdleten **set-AzNetworkSecurityGroup** anger mål tillståndet för en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="7aca2-106">The **Set-AzNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="7aca2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7aca2-107">EXAMPLES</span></span>

### <span data-ttu-id="7aca2-108">Exempel 1: Ange mål tillstånd för en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="7aca2-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="7aca2-109">Det här kommandot hämtar Azure nätverks säkerhets gruppen med namnet Nsg1 och lägger till en nätverks säkerhets regel med namnet Rdp-Rule för att tillåta Internet trafik på port 3389 till det hämtade objektet nätverks säkerhets grupp med hjälp av Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7aca2-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="7aca2-110">Kommandot behåller den ändrade Azure Network Security-gruppen med **set-AzNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="7aca2-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="7aca2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7aca2-111">PARAMETERS</span></span>

### <span data-ttu-id="7aca2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7aca2-112">-AsJob</span></span>
<span data-ttu-id="7aca2-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7aca2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7aca2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aca2-114">-DefaultProfile</span></span>
<span data-ttu-id="7aca2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7aca2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aca2-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7aca2-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7aca2-117">Ett nätverks säkerhets grupp objekt som representerar mål tillståndet där cmdleten ställer in nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="7aca2-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="7aca2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aca2-118">CommonParameters</span></span>
<span data-ttu-id="7aca2-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aca2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aca2-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aca2-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aca2-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7aca2-121">INPUTS</span></span>

### <span data-ttu-id="7aca2-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7aca2-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="7aca2-123">Parametern ' NetworkSecurityGroup ' godkänner värdet av typen ' PSNetworkSecurityGroup ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7aca2-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="7aca2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7aca2-124">OUTPUTS</span></span>

### <span data-ttu-id="7aca2-125">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7aca2-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="7aca2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7aca2-126">NOTES</span></span>

## <span data-ttu-id="7aca2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7aca2-127">RELATED LINKS</span></span>

[<span data-ttu-id="7aca2-128">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7aca2-128">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="7aca2-129">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7aca2-129">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="7aca2-130">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7aca2-130">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


