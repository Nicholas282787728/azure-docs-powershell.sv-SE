---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 78380af20ce5905b5c004424c1e17ac977de40ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747713"
---
# <span data-ttu-id="3c61f-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c61f-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="3c61f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c61f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c61f-103">Uppdaterar en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="3c61f-103">Updates a network security group.</span></span>

## <span data-ttu-id="3c61f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c61f-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c61f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c61f-105">DESCRIPTION</span></span>
<span data-ttu-id="3c61f-106">Cmdleten **set-AzNetworkSecurityGroup** uppdaterar en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="3c61f-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="3c61f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c61f-107">EXAMPLES</span></span>

### <span data-ttu-id="3c61f-108">Exempel 1: uppdatera en befintlig nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="3c61f-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="3c61f-109">Det här kommandot hämtar Azure nätverks säkerhets gruppen med namnet Nsg1 och lägger till en nätverks säkerhets regel med namnet Rdp-Rule för att tillåta Internet trafik på port 3389 till det hämtade objektet nätverks säkerhets grupp med hjälp av Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="3c61f-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="3c61f-110">Kommandot behåller den ändrade Azure Network Security-gruppen med **set-AzNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="3c61f-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="3c61f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c61f-111">PARAMETERS</span></span>

### <span data-ttu-id="3c61f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c61f-112">-AsJob</span></span>
<span data-ttu-id="3c61f-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3c61f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c61f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c61f-114">-DefaultProfile</span></span>
<span data-ttu-id="3c61f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c61f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c61f-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c61f-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3c61f-117">Anger ett nätverks säkerhets grupp objekt som representerar tillståndet som nätverks säkerhets gruppen ska ställas in för.</span><span class="sxs-lookup"><span data-stu-id="3c61f-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="3c61f-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3c61f-118">-Confirm</span></span>
<span data-ttu-id="3c61f-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c61f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c61f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c61f-120">-WhatIf</span></span>
<span data-ttu-id="3c61f-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3c61f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c61f-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3c61f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c61f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c61f-123">CommonParameters</span></span>
<span data-ttu-id="3c61f-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c61f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c61f-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c61f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c61f-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c61f-126">INPUTS</span></span>

### <span data-ttu-id="3c61f-127">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c61f-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="3c61f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c61f-128">OUTPUTS</span></span>

### <span data-ttu-id="3c61f-129">Microsoft. Azure. commands. Networks. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c61f-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="3c61f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c61f-130">NOTES</span></span>

## <span data-ttu-id="3c61f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c61f-131">RELATED LINKS</span></span>

[<span data-ttu-id="3c61f-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c61f-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="3c61f-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c61f-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="3c61f-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3c61f-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


