---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757849"
---
# <span data-ttu-id="ff3b4-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ff3b4-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="ff3b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3b4-103">Får en Azure-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff3b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff3b4-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff3b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff3b4-105">DESCRIPTION</span></span>
<span data-ttu-id="ff3b4-106">Cmdleten **Get-AzureRmFirewall** hämtar en eller flera brand väggar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="ff3b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff3b4-107">EXAMPLES</span></span>

### <span data-ttu-id="ff3b4-108">1: Hämta alla brand väggar i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ff3b4-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="ff3b4-109">I det här exemplet hämtas alla brand väggar i resurs gruppen "rgName".</span><span class="sxs-lookup"><span data-stu-id="ff3b4-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="ff3b4-110">2: Hämta en brand vägg efter namn</span><span class="sxs-lookup"><span data-stu-id="ff3b4-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="ff3b4-111">I det här exemplet hämtas brand väggen med namnet "azFw" i resurs gruppen "rgName".</span><span class="sxs-lookup"><span data-stu-id="ff3b4-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="ff3b4-112">3: Hämta en brand vägg och Lägg till en program regel samling i brand väggen</span><span class="sxs-lookup"><span data-stu-id="ff3b4-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="ff3b4-113">I det här exemplet hämtas en brand vägg och läggs sedan till i brand väggen genom att anropa metoden AddApplicationRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="ff3b4-114">4: Hämta en brand vägg och Lägg sedan till en nätverks regel samling i brand väggen</span><span class="sxs-lookup"><span data-stu-id="ff3b4-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="ff3b4-115">I det här exemplet hämtas en brand vägg och en nätverks regel läggs till i brand väggen genom att anropa metoden AddNetworkRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="ff3b4-116">5: Hämta en brand vägg och hämta en samling med program regler efter namn från brand väggen</span><span class="sxs-lookup"><span data-stu-id="ff3b4-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="ff3b4-117">I det här exemplet hämtas en brand vägg och sedan får regel samlingen ett namn som anropar metod GetApplicationRuleCollectionByName på brand Väggs objekt.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="ff3b4-118">Namnet på regel samlingen för metod GetApplicationRuleCollectionByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="ff3b4-119">6: Hämta en brand vägg och hämta en nätverks regel samling efter namn från brand väggen</span><span class="sxs-lookup"><span data-stu-id="ff3b4-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="ff3b4-120">I det här exemplet hämtas en brand vägg och sedan får regel samlingen ett namn som anropar metod GetNetworkRuleCollectionByName på brand Väggs objekt.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="ff3b4-121">Namnet på regel samlingen för metod GetNetworkRuleCollectionByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="ff3b4-122">7: Hämta en brand vägg och ta sedan bort en samling med program regler efter namn från brand väggen</span><span class="sxs-lookup"><span data-stu-id="ff3b4-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="ff3b4-123">I det här exemplet hämtas en brand vägg och sedan tas en regel samling bort från namn, metod RemoveApplicationRuleCollectionByName på brand Väggs objekt.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="ff3b4-124">Namnet på regel samlingen för metod RemoveApplicationRuleCollectionByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="ff3b4-125">8: Hämta en brand vägg och ta sedan bort en nätverks regel samling efter namn från brand väggen</span><span class="sxs-lookup"><span data-stu-id="ff3b4-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="ff3b4-126">I det här exemplet hämtas en brand vägg och sedan tas en regel samling bort från namn, metod RemoveNetworkRuleCollectionByName på brand Väggs objekt.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="ff3b4-127">Namnet på regel samlingen för metod RemoveNetworkRuleCollectionByName är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="ff3b4-128">9: Hämta en brand vägg och tilldela sedan brand väggen</span><span class="sxs-lookup"><span data-stu-id="ff3b4-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="ff3b4-129">I det här exemplet hämtas en brand vägg och samtal för att starta brand Väggs tjänsten med den konfiguration (program-och nätverks regel samlingar) som är kopplade till brand väggen.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="ff3b4-130">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff3b4-130">PARAMETERS</span></span>

### <span data-ttu-id="ff3b4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3b4-131">-DefaultProfile</span></span>
<span data-ttu-id="ff3b4-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff3b4-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff3b4-133">-Name</span></span>
<span data-ttu-id="ff3b4-134">Anger namnet på den brand vägg som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3b4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff3b4-135">-ResourceGroupName</span></span>
<span data-ttu-id="ff3b4-136">Anger namnet på den resurs grupp som brand väggen tillhör.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3b4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3b4-137">CommonParameters</span></span>
<span data-ttu-id="ff3b4-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3b4-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff3b4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3b4-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff3b4-140">INPUTS</span></span>

### <span data-ttu-id="ff3b4-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="ff3b4-141">None</span></span>
<span data-ttu-id="ff3b4-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ff3b4-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff3b4-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff3b4-143">OUTPUTS</span></span>

### <span data-ttu-id="ff3b4-144">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ff3b4-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="ff3b4-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff3b4-145">NOTES</span></span>

## <span data-ttu-id="ff3b4-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff3b4-146">RELATED LINKS</span></span>

[<span data-ttu-id="ff3b4-147">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ff3b4-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="ff3b4-148">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ff3b4-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="ff3b4-149">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ff3b4-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
