---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 7937af38c7dd0becd57604a0a7c00e5d1f584e6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747740"
---
# <span data-ttu-id="d0e31-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d0e31-101">Set-AzFirewall</span></span>

## <span data-ttu-id="d0e31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0e31-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e31-103">Sparar en modifierad brand vägg.</span><span class="sxs-lookup"><span data-stu-id="d0e31-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="d0e31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0e31-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0e31-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0e31-105">DESCRIPTION</span></span>
<span data-ttu-id="d0e31-106">Cmdleten **set-AzFirewall** uppdaterar en Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="d0e31-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="d0e31-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0e31-107">EXAMPLES</span></span>

### <span data-ttu-id="d0e31-108">1: uppdatera prioritet för en regel samling för en brand Väggs program</span><span class="sxs-lookup"><span data-stu-id="d0e31-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="d0e31-109">Det här exemplet uppdaterar prioriteten för en befintlig regel samling av en Azure-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="d0e31-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="d0e31-110">Om du antar Azure Firewall "AzureFirewall" i resurs gruppen "RG" innehåller en program regel samling med namnet "ruleCollectionName", kommer de ovanstående kommandona att ändra prioriteten för den regel samlingen och uppdatera Azure Firewall efteråt.</span><span class="sxs-lookup"><span data-stu-id="d0e31-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="d0e31-111">Utan kommandot Set-AzFirewall återspeglas inte alla åtgärder som utförs på det lokala $azFw-objektet på servern.</span><span class="sxs-lookup"><span data-stu-id="d0e31-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="d0e31-112">2: skapa en Azure-brandvägg och konfigurera en samling med program regler senare</span><span class="sxs-lookup"><span data-stu-id="d0e31-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="d0e31-113">I det här exemplet skapas en brand vägg först utan några program regel samlingar.</span><span class="sxs-lookup"><span data-stu-id="d0e31-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="d0e31-114">Därefter skapas en program regel-och program regel samling, och därefter ändras brand Väggs objekt i minnet utan att det påverkar den verkliga konfigurationen i molnet.</span><span class="sxs-lookup"><span data-stu-id="d0e31-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="d0e31-115">Set-AzFirewall måste anropas för att ändringarna ska synas i molnet.</span><span class="sxs-lookup"><span data-stu-id="d0e31-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="d0e31-116">3: uppdatera hotet Intels arbets läge i Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="d0e31-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="d0e31-117">I det här exemplet uppdateras hotet Intels arbets läge för Azure Firewall "AzureFirewall" i resurs gruppen "RG".</span><span class="sxs-lookup"><span data-stu-id="d0e31-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="d0e31-118">Utan kommandot Set-AzFirewall återspeglas inte alla åtgärder som utförs på det lokala $azFw-objektet på servern.</span><span class="sxs-lookup"><span data-stu-id="d0e31-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

## <span data-ttu-id="d0e31-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0e31-119">PARAMETERS</span></span>

### <span data-ttu-id="d0e31-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0e31-120">-AsJob</span></span>
<span data-ttu-id="d0e31-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d0e31-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0e31-122">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d0e31-122">-AzureFirewall</span></span>
<span data-ttu-id="d0e31-123">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d0e31-123">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e31-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e31-124">-DefaultProfile</span></span>
<span data-ttu-id="d0e31-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e31-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0e31-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0e31-126">-Confirm</span></span>
<span data-ttu-id="d0e31-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0e31-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e31-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e31-128">-WhatIf</span></span>
<span data-ttu-id="d0e31-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0e31-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0e31-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0e31-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e31-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e31-131">CommonParameters</span></span>
<span data-ttu-id="d0e31-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e31-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e31-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e31-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e31-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0e31-134">INPUTS</span></span>

### <span data-ttu-id="d0e31-135">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d0e31-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="d0e31-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0e31-136">OUTPUTS</span></span>

### <span data-ttu-id="d0e31-137">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d0e31-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="d0e31-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0e31-138">NOTES</span></span>

## <span data-ttu-id="d0e31-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0e31-139">RELATED LINKS</span></span>

[<span data-ttu-id="d0e31-140">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d0e31-140">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d0e31-141">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d0e31-141">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d0e31-142">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d0e31-142">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
