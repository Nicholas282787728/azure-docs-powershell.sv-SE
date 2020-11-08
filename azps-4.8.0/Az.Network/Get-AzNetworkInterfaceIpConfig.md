---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258292"
---
# <span data-ttu-id="83515-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83515-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="83515-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83515-102">SYNOPSIS</span></span>
<span data-ttu-id="83515-103">Hämtar en IP-konfiguration för nätverks gränssnitt för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="83515-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="83515-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83515-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83515-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83515-105">DESCRIPTION</span></span>
<span data-ttu-id="83515-106">Cmdleten **Get-AzNetworkInterfaceIPConfig** hämtar en IP-konfiguration för nätverks gränssnitt från ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="83515-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="83515-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83515-107">EXAMPLES</span></span>

### <span data-ttu-id="83515-108">1: Hämta en IP-konfiguration för ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="83515-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="83515-109">Det första kommandot får ett befintligt nätverks gränssnitt med namnet mynic och lagrar det i variabeln $nic 1.</span><span class="sxs-lookup"><span data-stu-id="83515-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="83515-110">Det andra kommandot får IP-konfigurationen som heter ipconfig1 för det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="83515-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="83515-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83515-111">PARAMETERS</span></span>

### <span data-ttu-id="83515-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83515-112">-DefaultProfile</span></span>
<span data-ttu-id="83515-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83515-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83515-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="83515-114">-Name</span></span>
<span data-ttu-id="83515-115">Anger namnet på den nätverks-IP-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="83515-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="83515-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="83515-116">-NetworkInterface</span></span>
<span data-ttu-id="83515-117">Anger ett **NetworkInterface** -objekt som innehåller nätverks-IP-konfigurationen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="83515-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83515-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83515-118">CommonParameters</span></span>
<span data-ttu-id="83515-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83515-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83515-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83515-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83515-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83515-121">INPUTS</span></span>

### <span data-ttu-id="83515-122">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="83515-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="83515-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83515-123">OUTPUTS</span></span>

### <span data-ttu-id="83515-124">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="83515-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="83515-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83515-125">NOTES</span></span>
* <span data-ttu-id="83515-126">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="83515-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="83515-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83515-127">RELATED LINKS</span></span>

[<span data-ttu-id="83515-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83515-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="83515-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83515-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="83515-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83515-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="83515-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="83515-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


