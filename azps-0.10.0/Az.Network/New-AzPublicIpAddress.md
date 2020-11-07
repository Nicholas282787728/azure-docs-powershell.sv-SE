---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 308758942a160b95f1a5bea89a476c15a0dcf003
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922102"
---
# <span data-ttu-id="dfae3-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dfae3-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="dfae3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfae3-102">SYNOPSIS</span></span>
<span data-ttu-id="dfae3-103">Skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="dfae3-103">Creates a public IP address.</span></span>

## <span data-ttu-id="dfae3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfae3-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfae3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfae3-105">DESCRIPTION</span></span>
<span data-ttu-id="dfae3-106">Cmdleten **New-AzPublicIpAddress** skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="dfae3-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="dfae3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfae3-107">EXAMPLES</span></span>

### <span data-ttu-id="dfae3-108">1: skapa en ny offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="dfae3-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="dfae3-109">Det här kommandot skapar en ny offentlig IP-adressresurs. En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="dfae3-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="dfae3-110">En offentlig IP-adress tilldelas omedelbart till den här resursen eftersom-AllocationMethod har angetts som "static".</span><span class="sxs-lookup"><span data-stu-id="dfae3-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="dfae3-111">Om den är angiven som "dynamisk" tilldelas en offentlig IP-adress endast när du startar (eller skapar) den associerade resursen (som en virtuell dator eller belastningsutjämnare).</span><span class="sxs-lookup"><span data-stu-id="dfae3-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="dfae3-112">2: skapa en offentlig IP-adress med omvänd FQDN</span><span class="sxs-lookup"><span data-stu-id="dfae3-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="dfae3-113">Det här kommandot skapar en ny offentlig IP-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="dfae3-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="dfae3-114">Med parametern-ReverseFqdn skapar Azure en DNS PTR-post (omvänd sökning) för den offentliga IP-adressen som tilldelats den här resursen och pekar på den $customFqdn som anges i kommandot.</span><span class="sxs-lookup"><span data-stu-id="dfae3-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="dfae3-115">Som en förutsättning måste $customFqdn (säg webapp.contoso.com) ha en DNS CNAME-post (forward-lookup) som pekar på $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="dfae3-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="dfae3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfae3-116">PARAMETERS</span></span>

### <span data-ttu-id="dfae3-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="dfae3-117">-AllocationMethod</span></span>
<span data-ttu-id="dfae3-118">Anger metoden för tilldelning av offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="dfae3-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="dfae3-119">De acceptabla värdena för den här parametern är: statiska eller dynamiska.</span><span class="sxs-lookup"><span data-stu-id="dfae3-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="dfae3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfae3-120">-AsJob</span></span>
<span data-ttu-id="dfae3-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dfae3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dfae3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfae3-122">-DefaultProfile</span></span>
<span data-ttu-id="dfae3-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfae3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfae3-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="dfae3-124">-DomainNameLabel</span></span>
<span data-ttu-id="dfae3-125">Anger det relativa DNS-namnet för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="dfae3-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="dfae3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="dfae3-126">-Force</span></span>
<span data-ttu-id="dfae3-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dfae3-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dfae3-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="dfae3-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="dfae3-129">Anger timeout för inaktivitet i minuter.</span><span class="sxs-lookup"><span data-stu-id="dfae3-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="dfae3-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="dfae3-130">-IpAddressVersion</span></span>
<span data-ttu-id="dfae3-131">Anger IP-adressens version.</span><span class="sxs-lookup"><span data-stu-id="dfae3-131">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="dfae3-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="dfae3-132">-Location</span></span>
<span data-ttu-id="dfae3-133">Anger i vilken region du vill skapa en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="dfae3-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="dfae3-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfae3-134">-Name</span></span>
<span data-ttu-id="dfae3-135">Anger namnet på den offentliga IP-adressen som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="dfae3-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dfae3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfae3-136">-ResourceGroupName</span></span>
<span data-ttu-id="dfae3-137">Anger namnet på den resurs grupp där en offentlig IP-adress ska skapas.</span><span class="sxs-lookup"><span data-stu-id="dfae3-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="dfae3-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="dfae3-138">-ReverseFqdn</span></span>
<span data-ttu-id="dfae3-139">Anger ett fullständigt kvalificerat domän namn (FQDN).</span><span class="sxs-lookup"><span data-stu-id="dfae3-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="dfae3-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="dfae3-140">-Sku</span></span>
<span data-ttu-id="dfae3-141">Det offentliga IP SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="dfae3-141">The public IP Sku name.</span></span>

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

### <span data-ttu-id="dfae3-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dfae3-142">-Tag</span></span>
<span data-ttu-id="dfae3-143">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="dfae3-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dfae3-144">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="dfae3-144">For example:</span></span>

<span data-ttu-id="dfae3-145">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="dfae3-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dfae3-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="dfae3-146">-Zone</span></span>
<span data-ttu-id="dfae3-147">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="dfae3-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="dfae3-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dfae3-148">-Confirm</span></span>
<span data-ttu-id="dfae3-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dfae3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfae3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfae3-150">-WhatIf</span></span>
<span data-ttu-id="dfae3-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dfae3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfae3-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dfae3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfae3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfae3-153">CommonParameters</span></span>
<span data-ttu-id="dfae3-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfae3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfae3-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfae3-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfae3-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfae3-156">INPUTS</span></span>

## <span data-ttu-id="dfae3-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfae3-157">OUTPUTS</span></span>

### <span data-ttu-id="dfae3-158">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dfae3-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="dfae3-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfae3-159">NOTES</span></span>

## <span data-ttu-id="dfae3-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfae3-160">RELATED LINKS</span></span>

[<span data-ttu-id="dfae3-161">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dfae3-161">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="dfae3-162">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dfae3-162">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="dfae3-163">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="dfae3-163">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
