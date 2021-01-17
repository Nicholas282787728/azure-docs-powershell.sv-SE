---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390807"
---
# <span data-ttu-id="47a4f-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="47a4f-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="47a4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="47a4f-103">Skapa en ny NAT-regel för Azure Firewall policy</span><span class="sxs-lookup"><span data-stu-id="47a4f-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="47a4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47a4f-104">SYNTAX</span></span>

### <span data-ttu-id="47a4f-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="47a4f-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47a4f-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="47a4f-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47a4f-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="47a4f-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47a4f-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="47a4f-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47a4f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47a4f-109">DESCRIPTION</span></span>
<span data-ttu-id="47a4f-110">Cmdleten **New-AzFirewallPolicyNatRule** skapar en NAT-regel för en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="47a4f-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="47a4f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47a4f-111">EXAMPLES</span></span>

### <span data-ttu-id="47a4f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="47a4f-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="47a4f-113">I det här exemplet skapas en NAT-regel med käll adress, protokoll, mål adress, målport, översatt adress och översatt port.</span><span class="sxs-lookup"><span data-stu-id="47a4f-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="47a4f-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="47a4f-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="47a4f-115">I det här exemplet skapas en NAT-regel med käll adress, protokoll, mål adress, målport, översatt FQDN och översatt port.</span><span class="sxs-lookup"><span data-stu-id="47a4f-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="47a4f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47a4f-116">PARAMETERS</span></span>

### <span data-ttu-id="47a4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a4f-117">-DefaultProfile</span></span>
<span data-ttu-id="47a4f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47a4f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47a4f-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="47a4f-119">-Description</span></span>
<span data-ttu-id="47a4f-120">Beskrivning av regeln</span><span class="sxs-lookup"><span data-stu-id="47a4f-120">The description of the rule</span></span>

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

### <span data-ttu-id="47a4f-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="47a4f-121">-DestinationAddress</span></span>
<span data-ttu-id="47a4f-122">Mål adresser för regeln.</span><span class="sxs-lookup"><span data-stu-id="47a4f-122">The destination addresses of the rule.</span></span> <span data-ttu-id="47a4f-123">Detta måste vara en offentlig IP-brand vägg.</span><span class="sxs-lookup"><span data-stu-id="47a4f-123">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a4f-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="47a4f-124">-DestinationPort</span></span>
<span data-ttu-id="47a4f-125">Mål portarna för regeln</span><span class="sxs-lookup"><span data-stu-id="47a4f-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a4f-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="47a4f-126">-Name</span></span>
<span data-ttu-id="47a4f-127">Namnet på listan över NAT-regler</span><span class="sxs-lookup"><span data-stu-id="47a4f-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="47a4f-128">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="47a4f-128">-Protocol</span></span>
<span data-ttu-id="47a4f-129">Regelns protokoll</span><span class="sxs-lookup"><span data-stu-id="47a4f-129">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a4f-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="47a4f-130">-SourceAddress</span></span>
<span data-ttu-id="47a4f-131">Käll adresserna för regeln</span><span class="sxs-lookup"><span data-stu-id="47a4f-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a4f-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="47a4f-132">-SourceIpGroup</span></span>
<span data-ttu-id="47a4f-133">Ipgroups regelns källkod</span><span class="sxs-lookup"><span data-stu-id="47a4f-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a4f-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="47a4f-134">-TranslatedAddress</span></span>
<span data-ttu-id="47a4f-135">Den översatta adressen för denna NAT-regel</span><span class="sxs-lookup"><span data-stu-id="47a4f-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a4f-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="47a4f-136">-TranslatedFqdn</span></span>
<span data-ttu-id="47a4f-137">Den översatta FQDN för denna NAT-regel</span><span class="sxs-lookup"><span data-stu-id="47a4f-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a4f-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="47a4f-138">-TranslatedPort</span></span>
<span data-ttu-id="47a4f-139">Den översatta porten för denna NAT-regel</span><span class="sxs-lookup"><span data-stu-id="47a4f-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="47a4f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a4f-140">CommonParameters</span></span>
<span data-ttu-id="47a4f-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a4f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a4f-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47a4f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a4f-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47a4f-143">INPUTS</span></span>

### <span data-ttu-id="47a4f-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="47a4f-144">None</span></span>

## <span data-ttu-id="47a4f-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47a4f-145">OUTPUTS</span></span>

### <span data-ttu-id="47a4f-146">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="47a4f-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="47a4f-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47a4f-147">NOTES</span></span>

## <span data-ttu-id="47a4f-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47a4f-148">RELATED LINKS</span></span>
