---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090190"
---
# <span data-ttu-id="46583-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="46583-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="46583-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46583-102">SYNOPSIS</span></span>
<span data-ttu-id="46583-103">Skapar en Azure SQL-instanskonstruktor.</span><span class="sxs-lookup"><span data-stu-id="46583-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="46583-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46583-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46583-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46583-105">DESCRIPTION</span></span>
<span data-ttu-id="46583-106">Cmdleten **New-AzSqlInstancePool** skapar en Azure SQL instance-pool.</span><span class="sxs-lookup"><span data-stu-id="46583-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="46583-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46583-107">EXAMPLES</span></span>

### <span data-ttu-id="46583-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="46583-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="46583-109">Det här kommandot skapar en ny Azure SQL-instans.</span><span class="sxs-lookup"><span data-stu-id="46583-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="46583-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46583-110">PARAMETERS</span></span>

### <span data-ttu-id="46583-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46583-111">-AsJob</span></span>
<span data-ttu-id="46583-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="46583-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46583-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="46583-113">-ComputeGeneration</span></span>
<span data-ttu-id="46583-114">Uppgenereringen av en instans.</span><span class="sxs-lookup"><span data-stu-id="46583-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="46583-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46583-115">-DefaultProfile</span></span>
<span data-ttu-id="46583-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46583-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46583-117">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="46583-117">-Edition</span></span>
<span data-ttu-id="46583-118">Versionen för entitetsinstansen.</span><span class="sxs-lookup"><span data-stu-id="46583-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="46583-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="46583-119">-LicenseType</span></span>
<span data-ttu-id="46583-120">Avgör vilken licens typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="46583-120">Determines which License Type to use.</span></span>
<span data-ttu-id="46583-121">Möjliga värden är BasePrice (med AHB rabatt) och LicenseIncluded (utan AHB rabatt).</span><span class="sxs-lookup"><span data-stu-id="46583-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="46583-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="46583-122">-Location</span></span>
<span data-ttu-id="46583-123">Platsen där du vill skapa instansen.</span><span class="sxs-lookup"><span data-stu-id="46583-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="46583-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="46583-124">-Name</span></span>
<span data-ttu-id="46583-125">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="46583-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46583-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46583-126">-ResourceGroupName</span></span>
<span data-ttu-id="46583-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="46583-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46583-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="46583-128">-SubnetId</span></span>
<span data-ttu-id="46583-129">Det Subnet-ID som ska användas för att skapa en instans.</span><span class="sxs-lookup"><span data-stu-id="46583-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="46583-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="46583-130">-Tag</span></span>
<span data-ttu-id="46583-131">Taggarna som ska kopplas till förekomsten</span><span class="sxs-lookup"><span data-stu-id="46583-131">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46583-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="46583-132">-VCore</span></span>
<span data-ttu-id="46583-133">Bestämmer hur många VCore som ska kopplas till en instans.</span><span class="sxs-lookup"><span data-stu-id="46583-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46583-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="46583-134">-Confirm</span></span>
<span data-ttu-id="46583-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="46583-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46583-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46583-136">-WhatIf</span></span>
<span data-ttu-id="46583-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="46583-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46583-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="46583-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46583-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46583-139">CommonParameters</span></span>
<span data-ttu-id="46583-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46583-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46583-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46583-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46583-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46583-142">INPUTS</span></span>

### <span data-ttu-id="46583-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="46583-143">None</span></span>

## <span data-ttu-id="46583-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46583-144">OUTPUTS</span></span>

### <span data-ttu-id="46583-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="46583-145">System.Object</span></span>
## <span data-ttu-id="46583-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46583-146">NOTES</span></span>

## <span data-ttu-id="46583-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46583-147">RELATED LINKS</span></span>
