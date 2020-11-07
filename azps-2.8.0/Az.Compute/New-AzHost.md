---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: e10e60845c9aeb90b7c708a65f7d681d9894b022
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745102"
---
# <span data-ttu-id="867f8-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="867f8-101">New-AzHost</span></span>

## <span data-ttu-id="867f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="867f8-102">SYNOPSIS</span></span>
<span data-ttu-id="867f8-103">Skapar en värd.</span><span class="sxs-lookup"><span data-stu-id="867f8-103">Creates a  host.</span></span>

## <span data-ttu-id="867f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="867f8-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="867f8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="867f8-105">DESCRIPTION</span></span>
<span data-ttu-id="867f8-106">Denna cmdlet skapar en värd.</span><span class="sxs-lookup"><span data-stu-id="867f8-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="867f8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="867f8-107">EXAMPLES</span></span>

### <span data-ttu-id="867f8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="867f8-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="867f8-109">Det här kommandot skapar en värd med angiven SKU i den angivna värd gruppen och den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="867f8-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="867f8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="867f8-110">PARAMETERS</span></span>

### <span data-ttu-id="867f8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="867f8-111">-AsJob</span></span>
<span data-ttu-id="867f8-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="867f8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="867f8-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="867f8-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="867f8-114">Anger om värden ska ersättas automatiskt om det uppstår ett fel.</span><span class="sxs-lookup"><span data-stu-id="867f8-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="867f8-115">Värdet är standardvärdet för ' true ' när det inte anges.</span><span class="sxs-lookup"><span data-stu-id="867f8-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867f8-116">-DefaultProfile</span></span>
<span data-ttu-id="867f8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="867f8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="867f8-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="867f8-118">-HostGroupName</span></span>
<span data-ttu-id="867f8-119">Anger namnet på värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="867f8-119">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="867f8-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="867f8-120">-LicenseType</span></span>
<span data-ttu-id="867f8-121">Anger vilken program varu licens typ som ska användas för de virtuella datorerna som distribueras på värden.</span><span class="sxs-lookup"><span data-stu-id="867f8-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="867f8-122">Möjliga värden är: ingen, Windows_Server_Hybrid och Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="867f8-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="867f8-123">Standardvärdet är inget.</span><span class="sxs-lookup"><span data-stu-id="867f8-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867f8-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="867f8-124">-Location</span></span>
<span data-ttu-id="867f8-125">Anger platsen.</span><span class="sxs-lookup"><span data-stu-id="867f8-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867f8-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="867f8-126">-Name</span></span>
<span data-ttu-id="867f8-127">Anger namnet på värden.</span><span class="sxs-lookup"><span data-stu-id="867f8-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="867f8-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="867f8-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="867f8-129">Anger antalet Platform Fault-domäner för värden.</span><span class="sxs-lookup"><span data-stu-id="867f8-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="867f8-130">Sedan är minimivärdet 0 och maximivärdet är 2.</span><span class="sxs-lookup"><span data-stu-id="867f8-130">Then minimum value is 0 and the maximum value is 2.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867f8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867f8-131">-ResourceGroupName</span></span>
<span data-ttu-id="867f8-132">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="867f8-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="867f8-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="867f8-133">-Sku</span></span>
<span data-ttu-id="867f8-134">Anger namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="867f8-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="867f8-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="867f8-135">-Tag</span></span>
<span data-ttu-id="867f8-136">Anger taggar.</span><span class="sxs-lookup"><span data-stu-id="867f8-136">Specifies Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867f8-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="867f8-137">-Confirm</span></span>
<span data-ttu-id="867f8-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="867f8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="867f8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="867f8-139">-WhatIf</span></span>
<span data-ttu-id="867f8-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="867f8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="867f8-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="867f8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="867f8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867f8-142">CommonParameters</span></span>
<span data-ttu-id="867f8-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="867f8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867f8-144">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="867f8-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867f8-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="867f8-145">INPUTS</span></span>

### <span data-ttu-id="867f8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="867f8-146">System.String</span></span>

## <span data-ttu-id="867f8-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="867f8-147">OUTPUTS</span></span>

### <span data-ttu-id="867f8-148">Microsoft. Azure. commands. Compute. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="867f8-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="867f8-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="867f8-149">NOTES</span></span>

## <span data-ttu-id="867f8-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="867f8-150">RELATED LINKS</span></span>
