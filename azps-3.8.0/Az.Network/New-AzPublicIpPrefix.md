---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 1f6931c294d26fbade402f2efefb4b722ef8203e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090978"
---
# <span data-ttu-id="6b612-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b612-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="6b612-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b612-102">SYNOPSIS</span></span>
<span data-ttu-id="6b612-103">Skapar ett offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="6b612-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="6b612-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b612-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b612-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b612-105">DESCRIPTION</span></span>
<span data-ttu-id="6b612-106">Cmdleten **New-AzPublicIpPrefix** skapar ett offentligt prefix.</span><span class="sxs-lookup"><span data-stu-id="6b612-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="6b612-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b612-107">EXAMPLES</span></span>

### <span data-ttu-id="6b612-108">1: skapa ett nytt offentligt IP-prefix</span><span class="sxs-lookup"><span data-stu-id="6b612-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="6b612-109">Det här kommandot skapar en ny offentlig IP-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="6b612-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="6b612-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b612-110">PARAMETERS</span></span>

### <span data-ttu-id="6b612-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b612-111">-AsJob</span></span>
<span data-ttu-id="6b612-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6b612-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b612-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b612-113">-DefaultProfile</span></span>
<span data-ttu-id="6b612-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b612-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b612-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6b612-115">-Force</span></span>
<span data-ttu-id="6b612-116">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="6b612-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6b612-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="6b612-117">-IpAddressVersion</span></span>
<span data-ttu-id="6b612-118">Den offentliga IP-adress versionen.</span><span class="sxs-lookup"><span data-stu-id="6b612-118">The public IP address version.</span></span>

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

### <span data-ttu-id="6b612-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="6b612-119">-IpTag</span></span>
<span data-ttu-id="6b612-120">IpTag-lista.</span><span class="sxs-lookup"><span data-stu-id="6b612-120">IpTag List.</span></span>

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

### <span data-ttu-id="6b612-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="6b612-121">-Location</span></span>
<span data-ttu-id="6b612-122">Platsen för offentlig IP-prefix.</span><span class="sxs-lookup"><span data-stu-id="6b612-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="6b612-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6b612-123">-Name</span></span>
<span data-ttu-id="6b612-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="6b612-124">The resource name.</span></span>

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

### <span data-ttu-id="6b612-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="6b612-125">-PrefixLength</span></span>
<span data-ttu-id="6b612-126">PublicIPPrefix längd</span><span class="sxs-lookup"><span data-stu-id="6b612-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="6b612-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b612-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b612-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6b612-128">The resource group name.</span></span>

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

### <span data-ttu-id="6b612-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="6b612-129">-Sku</span></span>
<span data-ttu-id="6b612-130">SKU-namnet för offentlig IP-prefix.</span><span class="sxs-lookup"><span data-stu-id="6b612-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="6b612-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6b612-131">-Tag</span></span>
<span data-ttu-id="6b612-132">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="6b612-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6b612-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="6b612-133">-Zone</span></span>
<span data-ttu-id="6b612-134">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="6b612-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="6b612-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b612-135">-Confirm</span></span>
<span data-ttu-id="6b612-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b612-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b612-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b612-137">-WhatIf</span></span>
<span data-ttu-id="6b612-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b612-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b612-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b612-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b612-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b612-140">CommonParameters</span></span>
<span data-ttu-id="6b612-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b612-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b612-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b612-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b612-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b612-143">INPUTS</span></span>

### <span data-ttu-id="6b612-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6b612-144">System.String</span></span>

### <span data-ttu-id="6b612-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="6b612-145">System.UInt16</span></span>

### <span data-ttu-id="6b612-146">Microsoft. Azure. commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="6b612-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="6b612-147">System. string []</span><span class="sxs-lookup"><span data-stu-id="6b612-147">System.String[]</span></span>

### <span data-ttu-id="6b612-148">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6b612-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6b612-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b612-149">OUTPUTS</span></span>

### <span data-ttu-id="6b612-150">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b612-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="6b612-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b612-151">NOTES</span></span>

## <span data-ttu-id="6b612-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b612-152">RELATED LINKS</span></span>

[<span data-ttu-id="6b612-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b612-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="6b612-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b612-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="6b612-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b612-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
