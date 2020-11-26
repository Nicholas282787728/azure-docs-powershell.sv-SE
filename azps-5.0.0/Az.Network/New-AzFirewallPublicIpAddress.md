---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271491"
---
# <span data-ttu-id="62b58-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="62b58-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="62b58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62b58-102">SYNOPSIS</span></span>
<span data-ttu-id="62b58-103">Det här är plats hållaren för den IP-adress som kan användas för multi-pip på Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="62b58-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="62b58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62b58-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62b58-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62b58-105">DESCRIPTION</span></span>
<span data-ttu-id="62b58-106">Det här är plats hållaren för den IP-adress som kan användas för multi-pip på Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="62b58-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="62b58-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62b58-107">EXAMPLES</span></span>

### <span data-ttu-id="62b58-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="62b58-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="62b58-109">$publicIp är plats hållaren för IP-adressen 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="62b58-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="62b58-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62b58-110">PARAMETERS</span></span>

### <span data-ttu-id="62b58-111">-Adress</span><span class="sxs-lookup"><span data-stu-id="62b58-111">-Address</span></span>
<span data-ttu-id="62b58-112">IP-adresserna för den brand vägg som är kopplad till navet</span><span class="sxs-lookup"><span data-stu-id="62b58-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="62b58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b58-113">-DefaultProfile</span></span>
<span data-ttu-id="62b58-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62b58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b58-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62b58-115">-Confirm</span></span>
<span data-ttu-id="62b58-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62b58-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62b58-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62b58-117">-WhatIf</span></span>
<span data-ttu-id="62b58-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62b58-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62b58-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62b58-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62b58-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b58-120">CommonParameters</span></span>
<span data-ttu-id="62b58-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b58-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b58-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62b58-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b58-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62b58-123">INPUTS</span></span>

### <span data-ttu-id="62b58-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="62b58-124">None</span></span>

## <span data-ttu-id="62b58-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62b58-125">OUTPUTS</span></span>

### <span data-ttu-id="62b58-126">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="62b58-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="62b58-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62b58-127">NOTES</span></span>

## <span data-ttu-id="62b58-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62b58-128">RELATED LINKS</span></span>