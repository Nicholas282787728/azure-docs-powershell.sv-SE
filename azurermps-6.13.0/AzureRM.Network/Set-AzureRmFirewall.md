---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572727"
---
# <span data-ttu-id="f20a4-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="f20a4-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="f20a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f20a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f20a4-103">Sparar en modifierad brand vägg.</span><span class="sxs-lookup"><span data-stu-id="f20a4-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f20a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f20a4-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f20a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f20a4-105">DESCRIPTION</span></span>
<span data-ttu-id="f20a4-106">Cmdleten **set-AzureRmFirewall** uppdaterar en Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="f20a4-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="f20a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f20a4-107">EXAMPLES</span></span>

### <span data-ttu-id="f20a4-108">1: uppdatera prioritet för en regel samling för en brand Väggs program</span><span class="sxs-lookup"><span data-stu-id="f20a4-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="f20a4-109">Det här exemplet uppdaterar prioriteten för en befintlig regel samling av en Azure-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="f20a4-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="f20a4-110">Om du antar Azure Firewall "AzureFirewall" i resurs gruppen "RG" innehåller en program regel samling med namnet "ruleCollectionName", kommer de ovanstående kommandona att ändra prioriteten för den regel samlingen och uppdatera Azure Firewall efteråt.</span><span class="sxs-lookup"><span data-stu-id="f20a4-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="f20a4-111">Utan kommandot Set-AzureRmFirewall återspeglas inte alla åtgärder som utförs på det lokala $azFw-objektet på servern.</span><span class="sxs-lookup"><span data-stu-id="f20a4-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="f20a4-112">2: skapa en Azure-brandvägg och konfigurera en samling med program regler senare</span><span class="sxs-lookup"><span data-stu-id="f20a4-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="f20a4-113">I det här exemplet skapas en brand vägg först utan några program regel samlingar.</span><span class="sxs-lookup"><span data-stu-id="f20a4-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="f20a4-114">Därefter skapas en program regel-och program regel samling, och därefter ändras brand Väggs objekt i minnet utan att det påverkar den verkliga konfigurationen i molnet.</span><span class="sxs-lookup"><span data-stu-id="f20a4-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="f20a4-115">Set-AzureRmFirewall måste anropas för att ändringarna ska synas i molnet.</span><span class="sxs-lookup"><span data-stu-id="f20a4-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="f20a4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f20a4-116">PARAMETERS</span></span>

### <span data-ttu-id="f20a4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f20a4-117">-AsJob</span></span>
<span data-ttu-id="f20a4-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f20a4-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20a4-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f20a4-119">-AzureFirewall</span></span>
<span data-ttu-id="f20a4-120">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f20a4-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f20a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20a4-121">-DefaultProfile</span></span>
<span data-ttu-id="f20a4-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f20a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f20a4-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f20a4-123">-Confirm</span></span>
<span data-ttu-id="f20a4-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f20a4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f20a4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f20a4-125">-WhatIf</span></span>
<span data-ttu-id="f20a4-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f20a4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f20a4-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f20a4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f20a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20a4-128">CommonParameters</span></span>
<span data-ttu-id="f20a4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f20a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20a4-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f20a4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20a4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f20a4-131">INPUTS</span></span>

### <span data-ttu-id="f20a4-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f20a4-132">PSAzureFirewall</span></span>
<span data-ttu-id="f20a4-133">Parametern ' AzureFirewall ' godkänner värdet av typen ' PSAzureFirewall ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f20a4-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="f20a4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f20a4-134">OUTPUTS</span></span>

### <span data-ttu-id="f20a4-135">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f20a4-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f20a4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f20a4-136">NOTES</span></span>

## <span data-ttu-id="f20a4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f20a4-137">RELATED LINKS</span></span>

[<span data-ttu-id="f20a4-138">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="f20a4-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="f20a4-139">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="f20a4-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="f20a4-140">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="f20a4-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
