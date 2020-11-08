---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 2e15819fe8b6b21b0f0c0751dc39736408606a7c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092483"
---
# <span data-ttu-id="cc611-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cc611-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="cc611-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc611-102">SYNOPSIS</span></span>
<span data-ttu-id="cc611-103">Skapar ett IP-konfigurationsobjekt för en behållare för nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="cc611-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="cc611-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc611-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc611-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc611-105">DESCRIPTION</span></span>
<span data-ttu-id="cc611-106">**New-AzContainerNicConfigIpConfig** cmdlet skapar en ny IP-konfiguration för en behållare för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="cc611-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="cc611-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc611-107">EXAMPLES</span></span>

### <span data-ttu-id="cc611-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cc611-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="cc611-109">De två första kommandona skapar och initierar ett VNet och ett undernät.</span><span class="sxs-lookup"><span data-stu-id="cc611-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="cc611-110">Det tredje kommandot skapar en IP-profil för en behållare som hänvisar till det skapade nätet.</span><span class="sxs-lookup"><span data-stu-id="cc611-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="cc611-111">Det fjärde kommandot skapar en behållare nätverks gränssnitts konfiguration med IP-konfigurationsfilen skapad i föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="cc611-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="cc611-112">Slutligen skapar det femte kommandot en nätverks profil som initierats med konfigurationen för behållaren nätverks gränssnitt som lagras i $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="cc611-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="cc611-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc611-113">PARAMETERS</span></span>

### <span data-ttu-id="cc611-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc611-114">-DefaultProfile</span></span>
<span data-ttu-id="cc611-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc611-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc611-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc611-116">-Name</span></span>
<span data-ttu-id="cc611-117">Namn på behållarens konfigurations profil för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="cc611-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="cc611-118">-Undernät</span><span class="sxs-lookup"><span data-stu-id="cc611-118">-Subnet</span></span>
<span data-ttu-id="cc611-119">Under</span><span class="sxs-lookup"><span data-stu-id="cc611-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc611-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cc611-120">-SubnetId</span></span>
<span data-ttu-id="cc611-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="cc611-121">SubnetId</span></span>

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

### <span data-ttu-id="cc611-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc611-122">-Confirm</span></span>
<span data-ttu-id="cc611-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc611-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc611-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc611-124">-WhatIf</span></span>
<span data-ttu-id="cc611-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc611-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc611-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc611-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc611-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc611-127">CommonParameters</span></span>
<span data-ttu-id="cc611-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc611-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc611-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc611-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc611-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc611-130">INPUTS</span></span>

### <span data-ttu-id="cc611-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="cc611-131">None</span></span>

## <span data-ttu-id="cc611-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc611-132">OUTPUTS</span></span>

### <span data-ttu-id="cc611-133">Microsoft. Azure. commands. Networks. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc611-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="cc611-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc611-134">NOTES</span></span>

## <span data-ttu-id="cc611-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc611-135">RELATED LINKS</span></span>

[<span data-ttu-id="cc611-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cc611-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)