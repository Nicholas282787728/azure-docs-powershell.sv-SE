---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399627"
---
# <span data-ttu-id="4fa9f-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4fa9f-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="4fa9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fa9f-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa9f-103">Det här är plats hållaren för den IP-adress som kan användas för multi-pip på Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="4fa9f-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="4fa9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fa9f-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fa9f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fa9f-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa9f-106">Det här är plats hållaren för den IP-adress som kan användas för multi-pip på Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="4fa9f-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="4fa9f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fa9f-107">EXAMPLES</span></span>

### <span data-ttu-id="4fa9f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4fa9f-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="4fa9f-109">$publicIp är plats hållaren för IP-adressen 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="4fa9f-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="4fa9f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fa9f-110">PARAMETERS</span></span>

### <span data-ttu-id="4fa9f-111">-Adress</span><span class="sxs-lookup"><span data-stu-id="4fa9f-111">-Address</span></span>
<span data-ttu-id="4fa9f-112">IP-adresserna för den brand vägg som är kopplad till navet</span><span class="sxs-lookup"><span data-stu-id="4fa9f-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="4fa9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa9f-113">-DefaultProfile</span></span>
<span data-ttu-id="4fa9f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4fa9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fa9f-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4fa9f-115">-Confirm</span></span>
<span data-ttu-id="4fa9f-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4fa9f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fa9f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fa9f-117">-WhatIf</span></span>
<span data-ttu-id="4fa9f-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4fa9f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fa9f-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4fa9f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fa9f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa9f-120">CommonParameters</span></span>
<span data-ttu-id="4fa9f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fa9f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa9f-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fa9f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa9f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fa9f-123">INPUTS</span></span>

### <span data-ttu-id="4fa9f-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="4fa9f-124">None</span></span>

## <span data-ttu-id="4fa9f-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fa9f-125">OUTPUTS</span></span>

### <span data-ttu-id="4fa9f-126">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4fa9f-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="4fa9f-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fa9f-127">NOTES</span></span>

## <span data-ttu-id="4fa9f-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fa9f-128">RELATED LINKS</span></span>
