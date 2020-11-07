---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757843"
---
# <span data-ttu-id="9111e-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9111e-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="9111e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9111e-102">SYNOPSIS</span></span>
<span data-ttu-id="9111e-103">Skapar ett offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="9111e-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9111e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9111e-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9111e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9111e-105">DESCRIPTION</span></span>
<span data-ttu-id="9111e-106">Cmdleten **New-AzureRmPublicIpPrefix** skapar ett offentligt prefix.</span><span class="sxs-lookup"><span data-stu-id="9111e-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="9111e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9111e-107">EXAMPLES</span></span>

### <span data-ttu-id="9111e-108">1: skapa ett nytt offentligt IP-prefix</span><span class="sxs-lookup"><span data-stu-id="9111e-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="9111e-109">Det här kommandot skapar en ny offentlig IP-prefixlängd.</span><span class="sxs-lookup"><span data-stu-id="9111e-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="9111e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9111e-110">PARAMETERS</span></span>

### <span data-ttu-id="9111e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9111e-111">-AsJob</span></span>
<span data-ttu-id="9111e-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9111e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9111e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9111e-113">-DefaultProfile</span></span>
<span data-ttu-id="9111e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9111e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9111e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9111e-115">-Force</span></span>
<span data-ttu-id="9111e-116">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="9111e-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="9111e-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="9111e-117">-IpAddressVersion</span></span>
<span data-ttu-id="9111e-118">Den offentliga IP-adress versionen.</span><span class="sxs-lookup"><span data-stu-id="9111e-118">The public IP address version.</span></span>

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

### <span data-ttu-id="9111e-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="9111e-119">-IpTag</span></span>
<span data-ttu-id="9111e-120">IpTag-lista.</span><span class="sxs-lookup"><span data-stu-id="9111e-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9111e-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="9111e-121">-Location</span></span>
<span data-ttu-id="9111e-122">Platsen för offentlig IP-prefix.</span><span class="sxs-lookup"><span data-stu-id="9111e-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="9111e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9111e-123">-Name</span></span>
<span data-ttu-id="9111e-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="9111e-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9111e-125">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="9111e-125">-PrefixLength</span></span>
<span data-ttu-id="9111e-126">PublicIPPrefix längd</span><span class="sxs-lookup"><span data-stu-id="9111e-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9111e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9111e-127">-ResourceGroupName</span></span>
<span data-ttu-id="9111e-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9111e-128">The resource group name.</span></span>

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

### <span data-ttu-id="9111e-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="9111e-129">-Sku</span></span>
<span data-ttu-id="9111e-130">SKU-namnet för offentlig IP-prefix.</span><span class="sxs-lookup"><span data-stu-id="9111e-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9111e-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9111e-131">-Tag</span></span>
<span data-ttu-id="9111e-132">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="9111e-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9111e-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="9111e-133">-Zone</span></span>
<span data-ttu-id="9111e-134">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="9111e-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="9111e-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9111e-135">-Confirm</span></span>
<span data-ttu-id="9111e-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9111e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9111e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9111e-137">-WhatIf</span></span>
<span data-ttu-id="9111e-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9111e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9111e-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9111e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9111e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9111e-140">CommonParameters</span></span>
<span data-ttu-id="9111e-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9111e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9111e-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9111e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9111e-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9111e-143">INPUTS</span></span>

### <span data-ttu-id="9111e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9111e-144">System.String</span></span>
<span data-ttu-id="9111e-145">System. UInt16 system. Collections. Genered. list `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] system. Collections. datagener</span><span class="sxs-lookup"><span data-stu-id="9111e-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="9111e-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9111e-146">OUTPUTS</span></span>

### <span data-ttu-id="9111e-147">Microsoft. Azure. commands. Networks. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9111e-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="9111e-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9111e-148">NOTES</span></span>

## <span data-ttu-id="9111e-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9111e-149">RELATED LINKS</span></span>
