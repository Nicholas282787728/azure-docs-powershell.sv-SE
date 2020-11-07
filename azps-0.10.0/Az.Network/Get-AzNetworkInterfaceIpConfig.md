---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 5936a7e3f15919e00fa052a2950fd31e69ca32fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922260"
---
# <span data-ttu-id="9c292-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c292-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="9c292-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c292-102">SYNOPSIS</span></span>
<span data-ttu-id="9c292-103">Hämtar en IP-konfiguration för nätverks gränssnitt för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="9c292-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="9c292-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c292-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c292-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c292-105">DESCRIPTION</span></span>
<span data-ttu-id="9c292-106">Cmdleten **Get-AzNetworkInterfaceIPConfig** hämtar en IP-konfiguration för nätverks gränssnitt från ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="9c292-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="9c292-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c292-107">EXAMPLES</span></span>

### <span data-ttu-id="9c292-108">1: Hämta en IP-konfiguration för ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="9c292-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="9c292-109">Det första kommandot får ett befintligt nätverks gränssnitt med namnet mynic och lagrar det i variabeln $nic 1.</span><span class="sxs-lookup"><span data-stu-id="9c292-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="9c292-110">Det andra kommandot får IP-konfigurationen som heter ipconfig1 för det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="9c292-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="9c292-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c292-111">PARAMETERS</span></span>

### <span data-ttu-id="9c292-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c292-112">-DefaultProfile</span></span>
<span data-ttu-id="9c292-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c292-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c292-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c292-114">-Name</span></span>
<span data-ttu-id="9c292-115">Anger namnet på den nätverks-IP-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9c292-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9c292-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9c292-116">-NetworkInterface</span></span>
<span data-ttu-id="9c292-117">Anger ett **NetworkInterface** -objekt som innehåller nätverks-IP-konfigurationen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9c292-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c292-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c292-118">CommonParameters</span></span>
<span data-ttu-id="9c292-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c292-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c292-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c292-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c292-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c292-121">INPUTS</span></span>

### <span data-ttu-id="9c292-122">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9c292-122">PSNetworkInterface</span></span>
<span data-ttu-id="9c292-123">Parametern ' NetworkInterface ' godkänner värdet av typen ' PSNetworkInterface ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9c292-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="9c292-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c292-124">OUTPUTS</span></span>

### <span data-ttu-id="9c292-125">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c292-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="9c292-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c292-126">NOTES</span></span>
* <span data-ttu-id="9c292-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="9c292-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9c292-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c292-128">RELATED LINKS</span></span>

[<span data-ttu-id="9c292-129">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c292-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9c292-130">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c292-130">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9c292-131">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c292-131">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9c292-132">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c292-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


