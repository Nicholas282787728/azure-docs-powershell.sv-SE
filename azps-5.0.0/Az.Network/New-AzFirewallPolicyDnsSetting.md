---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272893"
---
# <span data-ttu-id="4e777-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="4e777-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="4e777-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e777-102">SYNOPSIS</span></span>
<span data-ttu-id="4e777-103">Skapar en ny DNS-inställning för Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="4e777-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="4e777-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e777-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e777-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e777-105">DESCRIPTION</span></span>
<span data-ttu-id="4e777-106">Cmdleten **New-AzFirewallPolicyDnsSetting** skapar ett DNS Setting-objekt för Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="4e777-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="4e777-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e777-107">EXAMPLES</span></span>

### <span data-ttu-id="4e777-108">1. skapa en tom princip</span><span class="sxs-lookup"><span data-stu-id="4e777-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="4e777-109">I det här exemplet skapas ett DNS Setting-objekt med inställningen Aktivera DNS-proxy.</span><span class="sxs-lookup"><span data-stu-id="4e777-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="4e777-110">2. skapa en tom princip med ThreatIntel-läge</span><span class="sxs-lookup"><span data-stu-id="4e777-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="4e777-111">I det här exemplet skapas ett DNS Setting-objekt med inställningar för DNS-proxy och anpassade DNS-servrar.</span><span class="sxs-lookup"><span data-stu-id="4e777-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="4e777-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e777-112">PARAMETERS</span></span>

### <span data-ttu-id="4e777-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e777-113">-DefaultProfile</span></span>
<span data-ttu-id="4e777-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e777-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e777-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="4e777-115">-EnableProxy</span></span>
<span data-ttu-id="4e777-116">Aktivera DNS-proxy.</span><span class="sxs-lookup"><span data-stu-id="4e777-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="4e777-117">Den är som standard inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="4e777-117">By default it is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e777-118">-Server</span><span class="sxs-lookup"><span data-stu-id="4e777-118">-Server</span></span>
<span data-ttu-id="4e777-119">Listan med DNS-servrar</span><span class="sxs-lookup"><span data-stu-id="4e777-119">The list of DNS Servers</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e777-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e777-120">-Confirm</span></span>
<span data-ttu-id="4e777-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e777-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e777-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e777-122">-WhatIf</span></span>
<span data-ttu-id="4e777-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e777-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e777-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e777-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e777-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e777-125">CommonParameters</span></span>
<span data-ttu-id="4e777-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e777-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e777-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e777-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e777-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e777-128">INPUTS</span></span>

### <span data-ttu-id="4e777-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="4e777-129">None</span></span>

## <span data-ttu-id="4e777-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e777-130">OUTPUTS</span></span>

### <span data-ttu-id="4e777-131">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="4e777-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="4e777-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e777-132">NOTES</span></span>

## <span data-ttu-id="4e777-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e777-133">RELATED LINKS</span></span>