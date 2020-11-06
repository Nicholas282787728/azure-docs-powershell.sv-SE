---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9cbb814fde6d81449228a18913254cf807d5502c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574252"
---
# <span data-ttu-id="60b13-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="60b13-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="60b13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60b13-102">SYNOPSIS</span></span>
<span data-ttu-id="60b13-103">Tar bort en IP-konfiguration för nätverks gränssnitt från ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="60b13-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60b13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60b13-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60b13-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60b13-105">DESCRIPTION</span></span>
<span data-ttu-id="60b13-106">Cmdleten **Remove-AzureRmNetworkInterfaceIpConfig** tar bort en IP-konfiguration för nätverks gränssnitt från ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="60b13-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="60b13-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60b13-107">EXAMPLES</span></span>

### <span data-ttu-id="60b13-108">1: ta bort en IP-konfiguration från ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="60b13-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="60b13-109">Det första kommandot får ett nätverks gränssnitt med namnet mynic och lagrar det i variabeln $nic.</span><span class="sxs-lookup"><span data-stu-id="60b13-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="60b13-110">Det andra kommandot tar bort IP-konfigurationen som heter IPConfig-1 som är kopplad till det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="60b13-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="60b13-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60b13-111">PARAMETERS</span></span>

### <span data-ttu-id="60b13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b13-112">-DefaultProfile</span></span>
<span data-ttu-id="60b13-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60b13-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60b13-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="60b13-114">-Name</span></span>
<span data-ttu-id="60b13-115">Anger namnet på nätverks gränssnittets IP-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="60b13-115">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60b13-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="60b13-116">-NetworkInterface</span></span>
<span data-ttu-id="60b13-117">Anger ett **NetworkInterface** -objekt.</span><span class="sxs-lookup"><span data-stu-id="60b13-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="60b13-118">Det här objektet innehåller nätverks gränssnittets IP-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="60b13-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="60b13-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b13-119">CommonParameters</span></span>
<span data-ttu-id="60b13-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b13-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b13-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b13-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b13-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60b13-122">INPUTS</span></span>

### <span data-ttu-id="60b13-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="60b13-123">PSNetworkInterface</span></span>
<span data-ttu-id="60b13-124">Parametern ' NetworkInterface ' godkänner värdet av typen ' PSNetworkInterface ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="60b13-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="60b13-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60b13-125">OUTPUTS</span></span>

### <span data-ttu-id="60b13-126">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="60b13-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="60b13-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60b13-127">NOTES</span></span>
* <span data-ttu-id="60b13-128">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="60b13-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="60b13-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60b13-129">RELATED LINKS</span></span>

[<span data-ttu-id="60b13-130">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="60b13-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="60b13-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="60b13-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="60b13-132">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="60b13-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="60b13-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="60b13-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


