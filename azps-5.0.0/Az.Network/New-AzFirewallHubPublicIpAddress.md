---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271552"
---
# <span data-ttu-id="8c6a1-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8c6a1-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="8c6a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6a1-103">Offentlig IP-assoicated för brand väggen på virtuellt nav</span><span class="sxs-lookup"><span data-stu-id="8c6a1-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="8c6a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c6a1-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c6a1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c6a1-105">DESCRIPTION</span></span>
<span data-ttu-id="8c6a1-106">Offentlig IP-assoicated för brand väggen på virtuellt nav</span><span class="sxs-lookup"><span data-stu-id="8c6a1-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="8c6a1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c6a1-107">EXAMPLES</span></span>

### <span data-ttu-id="8c6a1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8c6a1-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="8c6a1-109">Detta skapar 2 offentliga IP-adresser på den brand vägg som är ansluten till det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="8c6a1-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="8c6a1-110">Detta skapar IP-adressen i Server delen. Vi kan inte tillhandahålla IP-adresser explicit för en ny brand vägg.</span><span class="sxs-lookup"><span data-stu-id="8c6a1-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="8c6a1-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8c6a1-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="8c6a1-112">Detta skapar en ny offentlig IP-adress i brand väggen genom att behålla $publicIp 1, $publicIp 2 som redan finns i brand väggen.</span><span class="sxs-lookup"><span data-stu-id="8c6a1-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="8c6a1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c6a1-113">PARAMETERS</span></span>

### <span data-ttu-id="8c6a1-114">-Adresser</span><span class="sxs-lookup"><span data-stu-id="8c6a1-114">-Addresses</span></span>
<span data-ttu-id="8c6a1-115">De offentliga IP-adresserna för den brand vägg som är ansluten till navet</span><span class="sxs-lookup"><span data-stu-id="8c6a1-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c6a1-116">-Antal</span><span class="sxs-lookup"><span data-stu-id="8c6a1-116">-Count</span></span>
<span data-ttu-id="8c6a1-117">Antalet offentliga IP-adresser</span><span class="sxs-lookup"><span data-stu-id="8c6a1-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c6a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6a1-118">-DefaultProfile</span></span>
<span data-ttu-id="8c6a1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c6a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c6a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6a1-120">CommonParameters</span></span>
<span data-ttu-id="8c6a1-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6a1-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c6a1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6a1-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c6a1-123">INPUTS</span></span>

### <span data-ttu-id="8c6a1-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="8c6a1-124">None</span></span>

## <span data-ttu-id="8c6a1-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c6a1-125">OUTPUTS</span></span>

### <span data-ttu-id="8c6a1-126">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="8c6a1-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="8c6a1-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c6a1-127">NOTES</span></span>

## <span data-ttu-id="8c6a1-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c6a1-128">RELATED LINKS</span></span>