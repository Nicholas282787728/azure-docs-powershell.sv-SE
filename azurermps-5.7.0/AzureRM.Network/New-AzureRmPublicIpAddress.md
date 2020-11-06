---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 98ea4632004787626237e5845f3c573b51a91934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584307"
---
# <span data-ttu-id="d9f1e-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9f1e-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="d9f1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f1e-103">Skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9f1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9f1e-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9f1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9f1e-105">DESCRIPTION</span></span>
<span data-ttu-id="d9f1e-106">Cmdleten **New-AzureRmPublicIpAddress** skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="d9f1e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9f1e-107">EXAMPLES</span></span>

### <span data-ttu-id="d9f1e-108">1: skapa en ny offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="d9f1e-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="d9f1e-109">Det här kommandot skapar en ny offentlig IP-adressresurs. En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="d9f1e-110">En offentlig IP-adress tilldelas omedelbart till den här resursen eftersom-AllocationMethod har angetts som "static".</span><span class="sxs-lookup"><span data-stu-id="d9f1e-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="d9f1e-111">Om den är angiven som "dynamisk" tilldelas en offentlig IP-adress endast när du startar (eller skapar) den associerade resursen (som en virtuell dator eller belastningsutjämnare).</span><span class="sxs-lookup"><span data-stu-id="d9f1e-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="d9f1e-112">2: skapa en offentlig IP-adress med omvänd FQDN</span><span class="sxs-lookup"><span data-stu-id="d9f1e-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="d9f1e-113">Det här kommandot skapar en ny offentlig IP-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="d9f1e-114">Med parametern-ReverseFqdn skapar Azure en DNS PTR-post (omvänd sökning) för den offentliga IP-adressen som tilldelats den här resursen och pekar på den $customFqdn som anges i kommandot.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="d9f1e-115">Som en förutsättning måste $customFqdn (säg webapp.contoso.com) ha en DNS CNAME-post (forward-lookup) som pekar på $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="d9f1e-116">3: skapa en ny offentlig IP-adress med IpTag</span><span class="sxs-lookup"><span data-stu-id="d9f1e-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="d9f1e-117">Det här kommandot skapar en ny offentlig IP-adressresurs. En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="d9f1e-118">En offentlig IP-adress tilldelas omedelbart till den här resursen eftersom-AllocationMethod har angetts som "static".</span><span class="sxs-lookup"><span data-stu-id="d9f1e-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="d9f1e-119">Om den är angiven som "dynamisk" tilldelas en offentlig IP-adress endast när du startar (eller skapar) den associerade resursen (som en virtuell dator eller belastningsutjämnare).</span><span class="sxs-lookup"><span data-stu-id="d9f1e-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="d9f1e-120">En Iptag används för att specifika taggar som är associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="d9f1e-121">Iptag kan anges med New-AzureRmPublicIpTag och skickas som indata via-IpTags.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

## <span data-ttu-id="d9f1e-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9f1e-122">PARAMETERS</span></span>

### <span data-ttu-id="d9f1e-123">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="d9f1e-123">-AllocationMethod</span></span>
<span data-ttu-id="d9f1e-124">Anger metoden för tilldelning av offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-124">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="d9f1e-125">De acceptabla värdena för den här parametern är: statiska eller dynamiska.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-125">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9f1e-126">-AsJob</span></span>
<span data-ttu-id="d9f1e-127">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d9f1e-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9f1e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f1e-128">-DefaultProfile</span></span>
<span data-ttu-id="d9f1e-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9f1e-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="d9f1e-130">-DomainNameLabel</span></span>
<span data-ttu-id="d9f1e-131">Anger det relativa DNS-namnet för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-131">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="d9f1e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d9f1e-132">-Force</span></span>
<span data-ttu-id="d9f1e-133">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9f1e-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d9f1e-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d9f1e-135">Anger timeout för inaktivitet i minuter.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-135">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-136">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="d9f1e-136">-IpAddressVersion</span></span>
<span data-ttu-id="d9f1e-137">Anger IP-adressens version.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-137">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-138">-IpTag</span><span class="sxs-lookup"><span data-stu-id="d9f1e-138">-IpTag</span></span>
<span data-ttu-id="d9f1e-139">IpTag-lista.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-139">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="d9f1e-140">-Location</span></span>
<span data-ttu-id="d9f1e-141">Anger i vilken region du vill skapa en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-141">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="d9f1e-142">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9f1e-142">-Name</span></span>
<span data-ttu-id="d9f1e-143">Anger namnet på den offentliga IP-adressen som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-143">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d9f1e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f1e-144">-ResourceGroupName</span></span>
<span data-ttu-id="d9f1e-145">Anger namnet på den resurs grupp där en offentlig IP-adress ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-145">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-146">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="d9f1e-146">-ReverseFqdn</span></span>
<span data-ttu-id="d9f1e-147">Anger ett fullständigt kvalificerat domän namn (FQDN).</span><span class="sxs-lookup"><span data-stu-id="d9f1e-147">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="d9f1e-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="d9f1e-148">-Sku</span></span>
<span data-ttu-id="d9f1e-149">Det offentliga IP SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-149">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d9f1e-150">-Tag</span></span>
<span data-ttu-id="d9f1e-151">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d9f1e-152">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="d9f1e-152">For example:</span></span>

<span data-ttu-id="d9f1e-153">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d9f1e-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="d9f1e-154">-Zone</span></span>
<span data-ttu-id="d9f1e-155">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-155">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9f1e-156">-Confirm</span></span>
<span data-ttu-id="d9f1e-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9f1e-158">-WhatIf</span></span>
<span data-ttu-id="d9f1e-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9f1e-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9f1e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f1e-161">CommonParameters</span></span>
<span data-ttu-id="d9f1e-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f1e-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9f1e-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f1e-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9f1e-164">INPUTS</span></span>

### <span data-ttu-id="d9f1e-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="d9f1e-165">None</span></span>
<span data-ttu-id="d9f1e-166">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d9f1e-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9f1e-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9f1e-167">OUTPUTS</span></span>

### <span data-ttu-id="d9f1e-168">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9f1e-168">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d9f1e-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9f1e-169">NOTES</span></span>

## <span data-ttu-id="d9f1e-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9f1e-170">RELATED LINKS</span></span>

[<span data-ttu-id="d9f1e-171">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9f1e-171">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d9f1e-172">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9f1e-172">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d9f1e-173">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9f1e-173">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
