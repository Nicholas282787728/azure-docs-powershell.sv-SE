---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
ms.openlocfilehash: 0a2157d006277aa491281c51f1c3b7a910b8a5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578900"
---
# <span data-ttu-id="463d3-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="463d3-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="463d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="463d3-102">SYNOPSIS</span></span>
<span data-ttu-id="463d3-103">Skapar ett IP-konfigurationsobjekt för en behållare för nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="463d3-103">Creates a container nic configuration ip configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="463d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="463d3-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="463d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="463d3-105">DESCRIPTION</span></span>
<span data-ttu-id="463d3-106">**New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet skapar en ny IP-konfiguration för en behållare för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="463d3-106">The **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="463d3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="463d3-107">EXAMPLES</span></span>

### <span data-ttu-id="463d3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="463d3-108">Example 1</span></span>
```powershell
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzureRmVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzureRmNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="463d3-109">De två första kommandona skapar och initierar ett VNet och ett undernät.</span><span class="sxs-lookup"><span data-stu-id="463d3-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="463d3-110">Det tredje kommandot skapar en IP-profil för en behållare som hänvisar till det skapade nätet.</span><span class="sxs-lookup"><span data-stu-id="463d3-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span>  <span data-ttu-id="463d3-111">Det fjärde kommandot skapar en behållare nätverks gränssnitts konfiguration med IP-konfigurationsfilen skapad i föregående kommando.</span><span class="sxs-lookup"><span data-stu-id="463d3-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="463d3-112">Slutligen skapar det femte kommandot en nätverks profil som initierats med konfigurationen för behållaren nätverks gränssnitt som lagras i $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="463d3-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="463d3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="463d3-113">PARAMETERS</span></span>

### <span data-ttu-id="463d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463d3-114">-DefaultProfile</span></span>
<span data-ttu-id="463d3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="463d3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="463d3-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="463d3-116">-Name</span></span>
<span data-ttu-id="463d3-117">Namn på behållarens konfigurations profil för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="463d3-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="463d3-118">-Undernät</span><span class="sxs-lookup"><span data-stu-id="463d3-118">-Subnet</span></span>
<span data-ttu-id="463d3-119">Under</span><span class="sxs-lookup"><span data-stu-id="463d3-119">Subnet</span></span>

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

### <span data-ttu-id="463d3-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="463d3-120">-SubnetId</span></span>
<span data-ttu-id="463d3-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="463d3-121">SubnetId</span></span>

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

### <span data-ttu-id="463d3-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="463d3-122">-Confirm</span></span>
<span data-ttu-id="463d3-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="463d3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="463d3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="463d3-124">-WhatIf</span></span>
<span data-ttu-id="463d3-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="463d3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="463d3-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="463d3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="463d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463d3-127">CommonParameters</span></span>
<span data-ttu-id="463d3-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463d3-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463d3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463d3-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="463d3-130">INPUTS</span></span>

### <span data-ttu-id="463d3-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="463d3-131">None</span></span>

## <span data-ttu-id="463d3-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="463d3-132">OUTPUTS</span></span>

### <span data-ttu-id="463d3-133">Microsoft. Azure. commands. Networks. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="463d3-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="463d3-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="463d3-134">NOTES</span></span>

## <span data-ttu-id="463d3-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="463d3-135">RELATED LINKS</span></span>
