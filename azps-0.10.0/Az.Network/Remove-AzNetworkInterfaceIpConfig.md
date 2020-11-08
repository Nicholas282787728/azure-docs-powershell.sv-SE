---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2ccb5f7117df8f959698c894915cedd3a5d4c7e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922021"
---
# <span data-ttu-id="9bac3-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bac3-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="9bac3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bac3-102">SYNOPSIS</span></span>
<span data-ttu-id="9bac3-103">Tar bort en IP-konfiguration för nätverks gränssnitt från ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="9bac3-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="9bac3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bac3-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bac3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bac3-105">DESCRIPTION</span></span>
<span data-ttu-id="9bac3-106">Cmdleten **Remove-AzNetworkInterfaceIpConfig** tar bort en IP-konfiguration för nätverks gränssnitt från ett Azure-nätverkskort.</span><span class="sxs-lookup"><span data-stu-id="9bac3-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="9bac3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bac3-107">EXAMPLES</span></span>

### <span data-ttu-id="9bac3-108">1: ta bort en IP-konfiguration från ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="9bac3-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="9bac3-109">Det första kommandot får ett nätverks gränssnitt med namnet mynic och lagrar det i variabeln $nic.</span><span class="sxs-lookup"><span data-stu-id="9bac3-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="9bac3-110">Det andra kommandot tar bort IP-konfigurationen som heter IPConfig-1 som är kopplad till det här nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="9bac3-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="9bac3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bac3-111">PARAMETERS</span></span>

### <span data-ttu-id="9bac3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bac3-112">-DefaultProfile</span></span>
<span data-ttu-id="9bac3-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bac3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bac3-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="9bac3-114">-Name</span></span>
<span data-ttu-id="9bac3-115">Anger namnet på nätverks gränssnittets IP-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9bac3-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="9bac3-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9bac3-116">-NetworkInterface</span></span>
<span data-ttu-id="9bac3-117">Anger ett **NetworkInterface** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9bac3-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="9bac3-118">Det här objektet innehåller nätverks gränssnittets IP-konfiguration som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9bac3-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="9bac3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bac3-119">CommonParameters</span></span>
<span data-ttu-id="9bac3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bac3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bac3-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bac3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bac3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bac3-122">INPUTS</span></span>

### <span data-ttu-id="9bac3-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9bac3-123">PSNetworkInterface</span></span>
<span data-ttu-id="9bac3-124">Parametern ' NetworkInterface ' godkänner värdet av typen ' PSNetworkInterface ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9bac3-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="9bac3-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bac3-125">OUTPUTS</span></span>

### <span data-ttu-id="9bac3-126">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9bac3-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="9bac3-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bac3-127">NOTES</span></span>
* <span data-ttu-id="9bac3-128">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="9bac3-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9bac3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bac3-129">RELATED LINKS</span></span>

[<span data-ttu-id="9bac3-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bac3-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9bac3-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bac3-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9bac3-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bac3-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9bac3-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9bac3-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)

