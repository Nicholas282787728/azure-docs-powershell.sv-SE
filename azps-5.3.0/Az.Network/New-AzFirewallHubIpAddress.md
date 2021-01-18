---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523277"
---
# <span data-ttu-id="39901-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="39901-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="39901-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39901-102">SYNOPSIS</span></span>
<span data-ttu-id="39901-103">IP-adresser assoicated till brand väggen på virtuellt nav</span><span class="sxs-lookup"><span data-stu-id="39901-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="39901-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39901-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39901-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39901-105">DESCRIPTION</span></span>
<span data-ttu-id="39901-106">IP-adresser assoicated till brand väggen på virtuellt nav.</span><span class="sxs-lookup"><span data-stu-id="39901-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="39901-107">Dessa kan vara offentliga och privata adresser</span><span class="sxs-lookup"><span data-stu-id="39901-107">These can be public and private addresses</span></span>

## <span data-ttu-id="39901-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39901-108">EXAMPLES</span></span>

### <span data-ttu-id="39901-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="39901-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="39901-110">I det här exemplet skapas ett nav-IP-adressprefix med antalet offentliga (public) IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="39901-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="39901-111">HubIPAddress-objektet är ssociated till brand väggen på det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="39901-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="39901-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39901-112">PARAMETERS</span></span>

### <span data-ttu-id="39901-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39901-113">-DefaultProfile</span></span>
<span data-ttu-id="39901-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39901-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39901-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="39901-115">-PrivateIPAddress</span></span>
<span data-ttu-id="39901-116">Den privata IP-adressen för den brand vägg som är kopplad till navet</span><span class="sxs-lookup"><span data-stu-id="39901-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="39901-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="39901-117">-PublicIPs</span></span>
<span data-ttu-id="39901-118">IP-adresserna för den brand vägg som är kopplad till navet</span><span class="sxs-lookup"><span data-stu-id="39901-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39901-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39901-119">-Confirm</span></span>
<span data-ttu-id="39901-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39901-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39901-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39901-121">-WhatIf</span></span>
<span data-ttu-id="39901-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39901-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39901-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39901-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39901-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39901-124">CommonParameters</span></span>
<span data-ttu-id="39901-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39901-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39901-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39901-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39901-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39901-127">INPUTS</span></span>

### <span data-ttu-id="39901-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="39901-128">None</span></span>

## <span data-ttu-id="39901-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39901-129">OUTPUTS</span></span>

### <span data-ttu-id="39901-130">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="39901-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="39901-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39901-131">NOTES</span></span>

## <span data-ttu-id="39901-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39901-132">RELATED LINKS</span></span>
