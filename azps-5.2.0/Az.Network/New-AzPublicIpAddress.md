---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391571"
---
# <span data-ttu-id="e9ff5-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e9ff5-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="e9ff5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ff5-103">Skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-103">Creates a public IP address.</span></span>

## <span data-ttu-id="e9ff5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9ff5-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9ff5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9ff5-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ff5-106">Cmdleten **New-AzPublicIpAddress** skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="e9ff5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9ff5-107">EXAMPLES</span></span>

### <span data-ttu-id="e9ff5-108">Exempel 1: skapa en ny offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="e9ff5-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="e9ff5-109">Det här kommandot skapar en ny offentlig IP-adressresurs. En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="e9ff5-110">En offentlig IP-adress tilldelas omedelbart till den här resursen eftersom-AllocationMethod har angetts som "static".</span><span class="sxs-lookup"><span data-stu-id="e9ff5-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="e9ff5-111">Om den är angiven som "dynamisk" tilldelas en offentlig IP-adress endast när du startar (eller skapar) den associerade resursen (som en virtuell dator eller belastningsutjämnare).</span><span class="sxs-lookup"><span data-stu-id="e9ff5-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="e9ff5-112">Exempel 2: skapa en offentlig IP-adress med omvänd FQDN</span><span class="sxs-lookup"><span data-stu-id="e9ff5-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="e9ff5-113">Det här kommandot skapar en ny offentlig IP-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="e9ff5-114">Med parametern-ReverseFqdn skapar Azure en DNS PTR-post (omvänd sökning) för den offentliga IP-adressen som tilldelats den här resursen och pekar på den $customFqdn som anges i kommandot.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="e9ff5-115">Som en förutsättning måste $customFqdn (säg webapp.contoso.com) ha en DNS CNAME-post (forward-lookup) som pekar på $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="e9ff5-116">Exempel 3: skapa en ny offentlig IP-adress med IpTag</span><span class="sxs-lookup"><span data-stu-id="e9ff5-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="e9ff5-117">Det här kommandot skapar en ny offentlig IP-adressresurs. En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="e9ff5-118">En offentlig IP-adress tilldelas omedelbart till den här resursen eftersom-AllocationMethod har angetts som "static".</span><span class="sxs-lookup"><span data-stu-id="e9ff5-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="e9ff5-119">Om den är angiven som "dynamisk" tilldelas en offentlig IP-adress endast när du startar (eller skapar) den associerade resursen (som en virtuell dator eller belastningsutjämnare).</span><span class="sxs-lookup"><span data-stu-id="e9ff5-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="e9ff5-120">En Iptag används för att specifika taggar som är associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="e9ff5-121">Iptag kan anges med New-AzPublicIpTag och skickas som indata via-IpTags.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="e9ff5-122">Exempel 4: skapa en ny offentlig IP-adress utifrån ett prefix</span><span class="sxs-lookup"><span data-stu-id="e9ff5-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="e9ff5-123">Det här kommandot skapar en ny offentlig IP-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="e9ff5-124">En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="e9ff5-125">En offentlig IP-adress tilldelas omedelbart till den här resursen från den angivna publicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="e9ff5-126">Det här alternativet stöds endast för "standard" SKU och "static"-AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="e9ff5-127">Exempel 5: skapa en ny global offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="e9ff5-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="e9ff5-128">Det här kommandot skapar en ny global offentlig IP-adressresurs. En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="e9ff5-129">En global offentlig IP-adress tilldelas omedelbart till den här resursen.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="e9ff5-130">Det här alternativet stöds endast för "standard" SKU och "static"-AllocationMethod.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="e9ff5-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9ff5-131">PARAMETERS</span></span>

### <span data-ttu-id="e9ff5-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="e9ff5-132">-AllocationMethod</span></span>
<span data-ttu-id="e9ff5-133">Anger metoden för tilldelning av offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="e9ff5-134">De acceptabla värdena för den här parametern är: statiska eller dynamiska.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="e9ff5-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9ff5-135">-AsJob</span></span>
<span data-ttu-id="e9ff5-136">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e9ff5-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9ff5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ff5-137">-DefaultProfile</span></span>
<span data-ttu-id="e9ff5-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9ff5-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="e9ff5-139">-DomainNameLabel</span></span>
<span data-ttu-id="e9ff5-140">Anger det relativa DNS-namnet för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="e9ff5-141">-Force</span><span class="sxs-lookup"><span data-stu-id="e9ff5-141">-Force</span></span>
<span data-ttu-id="e9ff5-142">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e9ff5-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e9ff5-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e9ff5-144">Anger timeout för inaktivitet i minuter.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="e9ff5-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e9ff5-145">-IpAddressVersion</span></span>
<span data-ttu-id="e9ff5-146">Anger IP-adressens version.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="e9ff5-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="e9ff5-147">-IpTag</span></span>
<span data-ttu-id="e9ff5-148">IpTag-lista.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-148">IpTag List.</span></span>

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

### <span data-ttu-id="e9ff5-149">-Plats</span><span class="sxs-lookup"><span data-stu-id="e9ff5-149">-Location</span></span>
<span data-ttu-id="e9ff5-150">Anger i vilken region du vill skapa en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="e9ff5-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9ff5-151">-Name</span></span>
<span data-ttu-id="e9ff5-152">Anger namnet på den offentliga IP-adressen som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e9ff5-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e9ff5-153">-PublicIpPrefix</span></span>
<span data-ttu-id="e9ff5-154">Anger den PSPublicIpPrefix som du vill tilldela den offentliga IP-adressen från.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="e9ff5-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9ff5-155">-ResourceGroupName</span></span>
<span data-ttu-id="e9ff5-156">Anger namnet på den resurs grupp där en offentlig IP-adress ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="e9ff5-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="e9ff5-157">-ReverseFqdn</span></span>
<span data-ttu-id="e9ff5-158">Anger ett fullständigt kvalificerat domän namn (FQDN).</span><span class="sxs-lookup"><span data-stu-id="e9ff5-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="e9ff5-159">-SKU</span><span class="sxs-lookup"><span data-stu-id="e9ff5-159">-Sku</span></span>
<span data-ttu-id="e9ff5-160">Det offentliga IP SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="e9ff5-161">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e9ff5-161">-Tag</span></span>
<span data-ttu-id="e9ff5-162">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e9ff5-163">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e9ff5-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e9ff5-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="e9ff5-164">-Tier</span></span>
<span data-ttu-id="e9ff5-165">Den offentliga IP-SKU-nivån.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-165">The public IP Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9ff5-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="e9ff5-166">-Zone</span></span>
<span data-ttu-id="e9ff5-167">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="e9ff5-168">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9ff5-168">-Confirm</span></span>
<span data-ttu-id="e9ff5-169">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9ff5-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9ff5-170">-WhatIf</span></span>
<span data-ttu-id="e9ff5-171">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9ff5-172">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9ff5-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ff5-173">CommonParameters</span></span>
<span data-ttu-id="e9ff5-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9ff5-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ff5-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9ff5-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ff5-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9ff5-176">INPUTS</span></span>

### <span data-ttu-id="e9ff5-177">System. String</span><span class="sxs-lookup"><span data-stu-id="e9ff5-177">System.String</span></span>

### <span data-ttu-id="e9ff5-178">Microsoft. Azure. commands. Network. Models. PSPublicIpTag []</span><span class="sxs-lookup"><span data-stu-id="e9ff5-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="e9ff5-179">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e9ff5-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="e9ff5-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e9ff5-180">System.Int32</span></span>

### <span data-ttu-id="e9ff5-181">System. string []</span><span class="sxs-lookup"><span data-stu-id="e9ff5-181">System.String[]</span></span>

### <span data-ttu-id="e9ff5-182">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="e9ff5-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e9ff5-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9ff5-183">OUTPUTS</span></span>

### <span data-ttu-id="e9ff5-184">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e9ff5-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="e9ff5-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9ff5-185">NOTES</span></span>

## <span data-ttu-id="e9ff5-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9ff5-186">RELATED LINKS</span></span>

[<span data-ttu-id="e9ff5-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e9ff5-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="e9ff5-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e9ff5-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="e9ff5-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e9ff5-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
