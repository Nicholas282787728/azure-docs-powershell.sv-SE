---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521842"
---
# <span data-ttu-id="18bc2-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="18bc2-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="18bc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="18bc2-103">Skapar ett offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="18bc2-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="18bc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18bc2-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18bc2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="18bc2-106">Cmdleten **New-AzPublicIpPrefix** skapar ett offentligt prefix.</span><span class="sxs-lookup"><span data-stu-id="18bc2-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="18bc2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18bc2-107">EXAMPLES</span></span>

### <span data-ttu-id="18bc2-108">Exempel 1: skapa ett nytt offentligt IP-prefix</span><span class="sxs-lookup"><span data-stu-id="18bc2-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="18bc2-109">Det här kommandot skapar en ny offentlig IP-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="18bc2-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="18bc2-110">Exempel 2: skapa ett nytt globalt offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="18bc2-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="18bc2-111">Det här kommandot skapar en ny global offentlig IP-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="18bc2-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="18bc2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18bc2-112">PARAMETERS</span></span>

### <span data-ttu-id="18bc2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18bc2-113">-AsJob</span></span>
<span data-ttu-id="18bc2-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="18bc2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18bc2-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="18bc2-115">-CustomIpPrefix</span></span>
<span data-ttu-id="18bc2-116">Den CustomIpPrefix som denna PublicIpPrefix ska kopplas till</span><span class="sxs-lookup"><span data-stu-id="18bc2-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18bc2-117">-DefaultProfile</span></span>
<span data-ttu-id="18bc2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18bc2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18bc2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="18bc2-119">-Force</span></span>
<span data-ttu-id="18bc2-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="18bc2-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="18bc2-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="18bc2-121">-IpAddressVersion</span></span>
<span data-ttu-id="18bc2-122">Den offentliga IP-adress versionen.</span><span class="sxs-lookup"><span data-stu-id="18bc2-122">The public IP address version.</span></span>

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

### <span data-ttu-id="18bc2-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="18bc2-123">-IpTag</span></span>
<span data-ttu-id="18bc2-124">IpTag-lista.</span><span class="sxs-lookup"><span data-stu-id="18bc2-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bc2-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="18bc2-125">-Location</span></span>
<span data-ttu-id="18bc2-126">Platsen för offentlig IP-prefix.</span><span class="sxs-lookup"><span data-stu-id="18bc2-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="18bc2-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="18bc2-127">-Name</span></span>
<span data-ttu-id="18bc2-128">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="18bc2-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bc2-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="18bc2-129">-PrefixLength</span></span>
<span data-ttu-id="18bc2-130">PublicIPPrefix längd</span><span class="sxs-lookup"><span data-stu-id="18bc2-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bc2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18bc2-131">-ResourceGroupName</span></span>
<span data-ttu-id="18bc2-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="18bc2-132">The resource group name.</span></span>

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

### <span data-ttu-id="18bc2-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="18bc2-133">-Sku</span></span>
<span data-ttu-id="18bc2-134">SKU-namnet för offentlig IP-prefix.</span><span class="sxs-lookup"><span data-stu-id="18bc2-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bc2-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="18bc2-135">-Tag</span></span>
<span data-ttu-id="18bc2-136">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="18bc2-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="18bc2-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="18bc2-137">-Tier</span></span>
<span data-ttu-id="18bc2-138">SKU-nivån för offentlig IP-prefix.</span><span class="sxs-lookup"><span data-stu-id="18bc2-138">The public IP Prefix Sku tier.</span></span>

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

### <span data-ttu-id="18bc2-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="18bc2-139">-Zone</span></span>
<span data-ttu-id="18bc2-140">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="18bc2-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="18bc2-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18bc2-141">-Confirm</span></span>
<span data-ttu-id="18bc2-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18bc2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18bc2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18bc2-143">-WhatIf</span></span>
<span data-ttu-id="18bc2-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18bc2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18bc2-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18bc2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18bc2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bc2-146">CommonParameters</span></span>
<span data-ttu-id="18bc2-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18bc2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bc2-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18bc2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bc2-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18bc2-149">INPUTS</span></span>

### <span data-ttu-id="18bc2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="18bc2-150">System.String</span></span>

### <span data-ttu-id="18bc2-151">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="18bc2-151">System.UInt16</span></span>

### <span data-ttu-id="18bc2-152">Microsoft. Azure. commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="18bc2-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="18bc2-153">System. string []</span><span class="sxs-lookup"><span data-stu-id="18bc2-153">System.String[]</span></span>

### <span data-ttu-id="18bc2-154">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="18bc2-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="18bc2-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18bc2-155">OUTPUTS</span></span>

### <span data-ttu-id="18bc2-156">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="18bc2-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="18bc2-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18bc2-157">NOTES</span></span>

## <span data-ttu-id="18bc2-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18bc2-158">RELATED LINKS</span></span>

[<span data-ttu-id="18bc2-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="18bc2-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="18bc2-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="18bc2-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="18bc2-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="18bc2-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
