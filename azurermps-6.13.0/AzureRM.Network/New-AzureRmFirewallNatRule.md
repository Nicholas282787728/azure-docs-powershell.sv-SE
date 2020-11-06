---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578888"
---
# <span data-ttu-id="6b6e3-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="6b6e3-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="6b6e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b6e3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b6e3-103">Skapar en brand Väggs NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b6e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b6e3-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b6e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b6e3-105">DESCRIPTION</span></span>
<span data-ttu-id="6b6e3-106">Cmdleten **New-AzureRmFirewallNatRule** skapar en NAT-regel för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="6b6e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b6e3-107">EXAMPLES</span></span>

### <span data-ttu-id="6b6e3-108">1: skapa en regel för att DNATa all TCP-trafik från 10.0.0.0/24 med mål 10.1.2.3:80 till destination 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="6b6e3-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="6b6e3-109">I det här exemplet skapas en regel som kommer att DNAT all trafik från 10.0.0.0/24 med mål 10.1.2.3:80 till 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="6b6e3-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="6b6e3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b6e3-110">PARAMETERS</span></span>

### <span data-ttu-id="6b6e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6e3-111">-DefaultProfile</span></span>
<span data-ttu-id="6b6e3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-113">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6b6e3-113">-Description</span></span>
<span data-ttu-id="6b6e3-114">Anger en valfri beskrivning av den här regeln.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="6b6e3-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6b6e3-115">-DestinationAddress</span></span>
<span data-ttu-id="6b6e3-116">Mål adresser för regeln.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-116">The destination addresses of the rule.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6b6e3-117">-DestinationPort</span></span>
<span data-ttu-id="6b6e3-118">Mål portarna för regeln</span><span class="sxs-lookup"><span data-stu-id="6b6e3-118">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="6b6e3-119">-Name</span></span>
<span data-ttu-id="6b6e3-120">Anger namnet på denna NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="6b6e3-121">Namnet måste vara unikt i en regel samling.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-121">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-122">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="6b6e3-122">-Protocol</span></span>
<span data-ttu-id="6b6e3-123">Anger typen av trafik som ska filtreras med den här regeln.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="6b6e3-124">De protokoll som stöds är TCP och UDP.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="6b6e3-125">Ett speciellt värde "any" tillåts, vilket betyder att det stämmer överens med både TCP och UDP men inte andra protokoll.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="6b6e3-126">-SourceAddress</span></span>
<span data-ttu-id="6b6e3-127">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="6b6e3-127">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="6b6e3-128">-TranslatedAddress</span></span>
<span data-ttu-id="6b6e3-129">Anger önskat resultat för adress översättningen</span><span class="sxs-lookup"><span data-stu-id="6b6e3-129">Specifies the desired result of the address translation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="6b6e3-130">-TranslatedPort</span></span>
<span data-ttu-id="6b6e3-131">Anger önskat resultat för port översättningen</span><span class="sxs-lookup"><span data-stu-id="6b6e3-131">Specifies the desired result of the port translation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b6e3-132">-Confirm</span></span>
<span data-ttu-id="6b6e3-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b6e3-134">-WhatIf</span></span>
<span data-ttu-id="6b6e3-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b6e3-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b6e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6e3-137">CommonParameters</span></span>
<span data-ttu-id="6b6e3-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6e3-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b6e3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6e3-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b6e3-140">INPUTS</span></span>

### <span data-ttu-id="6b6e3-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="6b6e3-141">None</span></span>
<span data-ttu-id="6b6e3-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6b6e3-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b6e3-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b6e3-143">OUTPUTS</span></span>

### <span data-ttu-id="6b6e3-144">Microsoft. Azure. commands. Networks. Models. PSFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="6b6e3-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="6b6e3-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b6e3-145">NOTES</span></span>

## <span data-ttu-id="6b6e3-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b6e3-146">RELATED LINKS</span></span>

[<span data-ttu-id="6b6e3-147">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="6b6e3-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="6b6e3-148">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6b6e3-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="6b6e3-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6b6e3-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
