---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 8437c6037b52fd274415a59bea6ee66a2f9c0588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575999"
---
# <span data-ttu-id="d58e2-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d58e2-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="d58e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d58e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d58e2-103">Skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d58e2-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d58e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d58e2-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d58e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d58e2-105">DESCRIPTION</span></span>
<span data-ttu-id="d58e2-106">Cmdleten **New-AzureRmPublicIpAddress** skapar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d58e2-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="d58e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d58e2-107">EXAMPLES</span></span>

### <span data-ttu-id="d58e2-108">1: skapa en ny offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="d58e2-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="d58e2-109">Det här kommandot skapar en ny offentlig IP-adressresurs. En DNS-post skapas för $dnsPrefix. $location. cloudapp.azure.com som pekar på den offentliga IP-adressen för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="d58e2-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="d58e2-110">En offentlig IP-adress tilldelas omedelbart till den här resursen eftersom-AllocationMethod har angetts som "static".</span><span class="sxs-lookup"><span data-stu-id="d58e2-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="d58e2-111">Om den är angiven som "dynamisk" tilldelas en offentlig IP-adress endast när du startar (eller skapar) den associerade resursen (som en virtuell dator eller belastningsutjämnare).</span><span class="sxs-lookup"><span data-stu-id="d58e2-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="d58e2-112">2: skapa en offentlig IP-adress med omvänd FQDN</span><span class="sxs-lookup"><span data-stu-id="d58e2-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="d58e2-113">Det här kommandot skapar en ny offentlig IP-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="d58e2-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="d58e2-114">Med parametern-ReverseFqdn skapar Azure en DNS PTR-post (omvänd sökning) för den offentliga IP-adressen som tilldelats den här resursen och pekar på den $customFqdn som anges i kommandot.</span><span class="sxs-lookup"><span data-stu-id="d58e2-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="d58e2-115">Som en förutsättning måste $customFqdn (säg webapp.contoso.com) ha en DNS CNAME-post (forward-lookup) som pekar på $dnsPrefix. $location. cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="d58e2-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="d58e2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d58e2-116">PARAMETERS</span></span>

### <span data-ttu-id="d58e2-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="d58e2-117">-AllocationMethod</span></span>
<span data-ttu-id="d58e2-118">Anger metoden för tilldelning av offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d58e2-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="d58e2-119">De acceptabla värdena för den här parametern är: statiska eller dynamiska.</span><span class="sxs-lookup"><span data-stu-id="d58e2-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="d58e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58e2-120">-DefaultProfile</span></span>
<span data-ttu-id="d58e2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d58e2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d58e2-122">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="d58e2-122">-DomainNameLabel</span></span>
<span data-ttu-id="d58e2-123">Anger det relativa DNS-namnet för en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d58e2-123">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="d58e2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d58e2-124">-Force</span></span>
<span data-ttu-id="d58e2-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d58e2-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d58e2-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d58e2-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d58e2-127">Anger timeout för inaktivitet i minuter.</span><span class="sxs-lookup"><span data-stu-id="d58e2-127">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="d58e2-128">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="d58e2-128">-IpAddressVersion</span></span>
<span data-ttu-id="d58e2-129">Anger IP-adressens version.</span><span class="sxs-lookup"><span data-stu-id="d58e2-129">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="d58e2-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="d58e2-130">-Location</span></span>
<span data-ttu-id="d58e2-131">Anger i vilken region du vill skapa en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d58e2-131">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="d58e2-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="d58e2-132">-Name</span></span>
<span data-ttu-id="d58e2-133">Anger namnet på den offentliga IP-adressen som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="d58e2-133">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d58e2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d58e2-134">-ResourceGroupName</span></span>
<span data-ttu-id="d58e2-135">Anger namnet på den resurs grupp där en offentlig IP-adress ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d58e2-135">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="d58e2-136">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="d58e2-136">-ReverseFqdn</span></span>
<span data-ttu-id="d58e2-137">Anger ett fullständigt kvalificerat domän namn (FQDN).</span><span class="sxs-lookup"><span data-stu-id="d58e2-137">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="d58e2-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="d58e2-138">-Sku</span></span>
<span data-ttu-id="d58e2-139">Det offentliga IP SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="d58e2-139">The public IP Sku name.</span></span>

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

### <span data-ttu-id="d58e2-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d58e2-140">-Tag</span></span>
<span data-ttu-id="d58e2-141">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d58e2-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d58e2-142">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="d58e2-142">For example:</span></span>

<span data-ttu-id="d58e2-143">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="d58e2-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d58e2-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="d58e2-144">-Zone</span></span>
<span data-ttu-id="d58e2-145">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="d58e2-145">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="d58e2-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d58e2-146">-Confirm</span></span>
<span data-ttu-id="d58e2-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d58e2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d58e2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d58e2-148">-WhatIf</span></span>
<span data-ttu-id="d58e2-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d58e2-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d58e2-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d58e2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d58e2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58e2-151">CommonParameters</span></span>
<span data-ttu-id="d58e2-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58e2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58e2-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58e2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58e2-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d58e2-154">INPUTS</span></span>

## <span data-ttu-id="d58e2-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d58e2-155">OUTPUTS</span></span>

### <span data-ttu-id="d58e2-156">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d58e2-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d58e2-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d58e2-157">NOTES</span></span>

## <span data-ttu-id="d58e2-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d58e2-158">RELATED LINKS</span></span>

[<span data-ttu-id="d58e2-159">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d58e2-159">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d58e2-160">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d58e2-160">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d58e2-161">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d58e2-161">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
