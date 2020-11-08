---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: c3f051e50966bc5ede86c9dafa00c2f4518dbf59
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090982"
---
# <span data-ttu-id="992c0-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="992c0-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="992c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="992c0-102">SYNOPSIS</span></span>
<span data-ttu-id="992c0-103">Skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="992c0-103">Creates a public IP address.</span></span>

## <span data-ttu-id="992c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="992c0-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-IpTag <PSPublicIpTag[]>]
 [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>] [-IdleTimeoutInMinutes <Int32>]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="992c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="992c0-105">DESCRIPTION</span></span>
<span data-ttu-id="992c0-106">Cmdleten **New-AzPublicIpAddress** skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="992c0-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="992c0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="992c0-107">EXAMPLES</span></span>

### <span data-ttu-id="992c0-108">1: skapa en ny offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="992c0-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="992c0-109">Det här kommandot skapar en ny offentlig IP-adressresurs. En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="992c0-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="992c0-110">En offentlig IP-adress tilldelas omedelbart till den här resursen eftersom-AllocationMethod har angetts som "static".</span><span class="sxs-lookup"><span data-stu-id="992c0-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="992c0-111">Om den är angiven som "dynamisk" tilldelas en offentlig IP-adress endast när du startar (eller skapar) den associerade resursen (som en virtuell dator eller belastningsutjämnare).</span><span class="sxs-lookup"><span data-stu-id="992c0-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="992c0-112">2: skapa en offentlig IP-adress med omvänd FQDN</span><span class="sxs-lookup"><span data-stu-id="992c0-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="992c0-113">Det här kommandot skapar en ny offentlig IP-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="992c0-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="992c0-114">Med parametern-ReverseFqdn skapar Azure en DNS PTR-post (omvänd sökning) för den offentliga IP-adressen som tilldelats den här resursen och pekar på den $customFqdn som anges i kommandot.</span><span class="sxs-lookup"><span data-stu-id="992c0-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="992c0-115">Som en förutsättning måste $customFqdn (säg webapp.contoso.com) ha en DNS CNAME-post (forward-lookup) som pekar på $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="992c0-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="992c0-116">3: skapa en ny offentlig IP-adress med IpTag</span><span class="sxs-lookup"><span data-stu-id="992c0-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="992c0-117">Det här kommandot skapar en ny offentlig IP-adressresurs. En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="992c0-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="992c0-118">En offentlig IP-adress tilldelas omedelbart till den här resursen eftersom-AllocationMethod har angetts som "static".</span><span class="sxs-lookup"><span data-stu-id="992c0-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="992c0-119">Om den är angiven som "dynamisk" tilldelas en offentlig IP-adress endast när du startar (eller skapar) den associerade resursen (som en virtuell dator eller belastningsutjämnare).</span><span class="sxs-lookup"><span data-stu-id="992c0-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="992c0-120">En Iptag används för att specifika taggar som är associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="992c0-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="992c0-121">Iptag kan anges med New-AzPublicIpTag och skickas som indata via-IpTags.</span><span class="sxs-lookup"><span data-stu-id="992c0-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="992c0-122">4: skapa en ny offentlig IP-adress utifrån ett prefix</span><span class="sxs-lookup"><span data-stu-id="992c0-122">4: Create a new public IP address from a Prefix</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="992c0-123">Det här kommandot skapar en ny offentlig IP-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="992c0-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="992c0-124">En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="992c0-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="992c0-125">En offentlig IP-adress tilldelas omedelbart till den här resursen från den angivna publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="992c0-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="992c0-126">Det här alternativet stöds endast för "standard" SKU och "static"-AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="992c0-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="992c0-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="992c0-127">PARAMETERS</span></span>

### <span data-ttu-id="992c0-128">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="992c0-128">-AllocationMethod</span></span>
<span data-ttu-id="992c0-129">Anger metoden för tilldelning av offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="992c0-129">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="992c0-130">De acceptabla värdena för den här parametern är: statiska eller dynamiska.</span><span class="sxs-lookup"><span data-stu-id="992c0-130">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="992c0-131">-AsJob</span></span>
<span data-ttu-id="992c0-132">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="992c0-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="992c0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992c0-133">-DefaultProfile</span></span>
<span data-ttu-id="992c0-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="992c0-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="992c0-135">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="992c0-135">-DomainNameLabel</span></span>
<span data-ttu-id="992c0-136">Anger det relativa DNS-namnet för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="992c0-136">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-137">-Force</span><span class="sxs-lookup"><span data-stu-id="992c0-137">-Force</span></span>
<span data-ttu-id="992c0-138">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="992c0-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="992c0-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="992c0-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="992c0-140">Anger timeout för inaktivitet i minuter.</span><span class="sxs-lookup"><span data-stu-id="992c0-140">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-141">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="992c0-141">-IpAddressVersion</span></span>
<span data-ttu-id="992c0-142">Anger IP-adressens version.</span><span class="sxs-lookup"><span data-stu-id="992c0-142">Specifies the version of the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-143">-IpTag</span><span class="sxs-lookup"><span data-stu-id="992c0-143">-IpTag</span></span>
<span data-ttu-id="992c0-144">IpTag-lista.</span><span class="sxs-lookup"><span data-stu-id="992c0-144">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-145">-Plats</span><span class="sxs-lookup"><span data-stu-id="992c0-145">-Location</span></span>
<span data-ttu-id="992c0-146">Anger i vilken region du vill skapa en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="992c0-146">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="992c0-147">-Name</span></span>
<span data-ttu-id="992c0-148">Anger namnet på den offentliga IP-adressen som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="992c0-148">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-149">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c0-149">-PublicIpPrefix</span></span>
<span data-ttu-id="992c0-150">Anger den PSPublicIpPrefix som du vill tilldela den offentliga IP-adressen från.</span><span class="sxs-lookup"><span data-stu-id="992c0-150">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="992c0-151">-ResourceGroupName</span></span>
<span data-ttu-id="992c0-152">Anger namnet på den resurs grupp där en offentlig IP-adress ska skapas.</span><span class="sxs-lookup"><span data-stu-id="992c0-152">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-153">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="992c0-153">-ReverseFqdn</span></span>
<span data-ttu-id="992c0-154">Anger ett fullständigt kvalificerat domän namn (FQDN).</span><span class="sxs-lookup"><span data-stu-id="992c0-154">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="992c0-155">-Sku</span></span>
<span data-ttu-id="992c0-156">Det offentliga IP SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="992c0-156">The public IP Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-157">-Tagg</span><span class="sxs-lookup"><span data-stu-id="992c0-157">-Tag</span></span>
<span data-ttu-id="992c0-158">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="992c0-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="992c0-159">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="992c0-159">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-160">-Zone</span><span class="sxs-lookup"><span data-stu-id="992c0-160">-Zone</span></span>
<span data-ttu-id="992c0-161">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="992c0-161">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992c0-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="992c0-162">-Confirm</span></span>
<span data-ttu-id="992c0-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="992c0-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="992c0-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="992c0-164">-WhatIf</span></span>
<span data-ttu-id="992c0-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="992c0-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="992c0-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="992c0-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="992c0-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992c0-167">CommonParameters</span></span>
<span data-ttu-id="992c0-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992c0-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992c0-169">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="992c0-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992c0-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="992c0-170">INPUTS</span></span>

### <span data-ttu-id="992c0-171">System. String</span><span class="sxs-lookup"><span data-stu-id="992c0-171">System.String</span></span>

### <span data-ttu-id="992c0-172">Microsoft. Azure. commands. Network. Models. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="992c0-172">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="992c0-173">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="992c0-173">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="992c0-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="992c0-174">System.Int32</span></span>

### <span data-ttu-id="992c0-175">System. string []</span><span class="sxs-lookup"><span data-stu-id="992c0-175">System.String[]</span></span>

### <span data-ttu-id="992c0-176">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="992c0-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="992c0-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="992c0-177">OUTPUTS</span></span>

### <span data-ttu-id="992c0-178">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="992c0-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="992c0-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="992c0-179">NOTES</span></span>

## <span data-ttu-id="992c0-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="992c0-180">RELATED LINKS</span></span>

[<span data-ttu-id="992c0-181">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="992c0-181">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="992c0-182">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="992c0-182">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="992c0-183">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="992c0-183">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
