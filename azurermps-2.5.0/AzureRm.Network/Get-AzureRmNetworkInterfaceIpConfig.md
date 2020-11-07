---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: c08bf4ac0344e58242f967df8166c15a241ea657
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931286"
---
# <span data-ttu-id="6f964-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f964-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="6f964-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f964-102">SYNOPSIS</span></span>
<span data-ttu-id="6f964-103">Hämtar en IP-konfiguration för nätverks gränssnitt för ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="6f964-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f964-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f964-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f964-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f964-105">DESCRIPTION</span></span>
<span data-ttu-id="6f964-106">Cmdleten **Get-AzureRmNetworkInterfaceIPConfig** hämtar en IP-konfiguration för nätverks gränssnitt från ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="6f964-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="6f964-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f964-107">EXAMPLES</span></span>

### <span data-ttu-id="6f964-108">1: Hämta en IP-konfiguration för ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="6f964-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="6f964-109">Det första kommandot får ett befintligt nätverks gränssnitt med namnet mynic och lagrar det i variabeln $nic 1.</span><span class="sxs-lookup"><span data-stu-id="6f964-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="6f964-110">Det andra kommandot får IP-konfigurationen som heter ipconfig1 för det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="6f964-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="6f964-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f964-111">PARAMETERS</span></span>

### <span data-ttu-id="6f964-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f964-112">-DefaultProfile</span></span>
<span data-ttu-id="6f964-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f964-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f964-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f964-114">-Name</span></span>
<span data-ttu-id="6f964-115">Anger namnet på den nätverks-IP-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="6f964-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f964-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6f964-116">-NetworkInterface</span></span>
<span data-ttu-id="6f964-117">Anger ett **NetworkInterface** -objekt som innehåller nätverks-IP-konfigurationen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="6f964-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f964-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f964-118">CommonParameters</span></span>
<span data-ttu-id="6f964-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f964-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f964-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f964-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f964-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f964-121">INPUTS</span></span>

### <span data-ttu-id="6f964-122">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6f964-122">PSNetworkInterface</span></span>
<span data-ttu-id="6f964-123">Parametern ' NetworkInterface ' godkänner värdet av typen ' PSNetworkInterface ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6f964-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="6f964-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f964-124">OUTPUTS</span></span>

### <span data-ttu-id="6f964-125">Microsoft. Azure. commands. Networks. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f964-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="6f964-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f964-126">NOTES</span></span>
* <span data-ttu-id="6f964-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="6f964-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6f964-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f964-128">RELATED LINKS</span></span>

[<span data-ttu-id="6f964-129">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f964-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6f964-130">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f964-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6f964-131">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f964-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="6f964-132">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f964-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


