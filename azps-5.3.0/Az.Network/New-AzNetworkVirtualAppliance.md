---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521867"
---
# <span data-ttu-id="4f5a4-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="4f5a4-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="4f5a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5a4-103">Skapa en resurs för virtuella nätverk enheter.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="4f5a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f5a4-104">SYNTAX</span></span>

### <span data-ttu-id="4f5a4-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4f5a4-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f5a4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f5a4-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f5a4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f5a4-107">DESCRIPTION</span></span>
<span data-ttu-id="4f5a4-108">Med kommandot New-AzNetworkVirtualAppliance skapas en resurs för virtuella nätverk enheter i Azure.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="4f5a4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f5a4-109">EXAMPLES</span></span>

### <span data-ttu-id="4f5a4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f5a4-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="4f5a4-111">Skapar en ny virtuell nätverks utrustnings resurs i resurs gruppen: testrg.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="4f5a4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f5a4-112">PARAMETERS</span></span>

### <span data-ttu-id="4f5a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f5a4-113">-AsJob</span></span>
<span data-ttu-id="4f5a4-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4f5a4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f5a4-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="4f5a4-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="4f5a4-116">Start konfigurationens BLOB-URL.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="4f5a4-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f5a4-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="4f5a4-118">Cloudinit konfiguration som oformaterad text.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="4f5a4-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="4f5a4-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="4f5a4-120">Cloudinit-URL för BLOB för konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="4f5a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5a4-121">-DefaultProfile</span></span>
<span data-ttu-id="4f5a4-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f5a4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4f5a4-123">-Force</span></span>
<span data-ttu-id="4f5a4-124">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="4f5a4-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4f5a4-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="4f5a4-125">-Identity</span></span>
<span data-ttu-id="4f5a4-126">Den hanterade identiteten.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5a4-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="4f5a4-127">-Location</span></span>
<span data-ttu-id="4f5a4-128">Den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-128">The public IP address location.</span></span>

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

### <span data-ttu-id="4f5a4-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f5a4-129">-Name</span></span>
<span data-ttu-id="4f5a4-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5a4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f5a4-131">-ResourceGroupName</span></span>
<span data-ttu-id="4f5a4-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5a4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f5a4-133">-ResourceId</span></span>
<span data-ttu-id="4f5a4-134">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5a4-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="4f5a4-135">-Sku</span></span>
<span data-ttu-id="4f5a4-136">SKU för den virtuella produkten.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5a4-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4f5a4-137">-Tag</span></span>
<span data-ttu-id="4f5a4-138">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4f5a4-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="4f5a4-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="4f5a4-140">ASN-numret för den virtuella produkten.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5a4-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="4f5a4-141">-VirtualHubId</span></span>
<span data-ttu-id="4f5a4-142">Resurs-ID för det virtuella navet.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="4f5a4-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f5a4-143">-Confirm</span></span>
<span data-ttu-id="4f5a4-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f5a4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f5a4-145">-WhatIf</span></span>
<span data-ttu-id="4f5a4-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f5a4-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f5a4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5a4-148">CommonParameters</span></span>
<span data-ttu-id="4f5a4-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5a4-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f5a4-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5a4-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f5a4-151">INPUTS</span></span>

### <span data-ttu-id="4f5a4-152">System. String</span><span class="sxs-lookup"><span data-stu-id="4f5a4-152">System.String</span></span>

### <span data-ttu-id="4f5a4-153">Microsoft. Azure. commands. Networks. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="4f5a4-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="4f5a4-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4f5a4-154">System.Int32</span></span>

### <span data-ttu-id="4f5a4-155">Microsoft. Azure. commands. Networks. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="4f5a4-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="4f5a4-156">System. string []</span><span class="sxs-lookup"><span data-stu-id="4f5a4-156">System.String[]</span></span>

### <span data-ttu-id="4f5a4-157">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4f5a4-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f5a4-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f5a4-158">OUTPUTS</span></span>

### <span data-ttu-id="4f5a4-159">Microsoft. Azure. commands. Networks. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="4f5a4-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="4f5a4-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f5a4-160">NOTES</span></span>

## <span data-ttu-id="4f5a4-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f5a4-161">RELATED LINKS</span></span>
