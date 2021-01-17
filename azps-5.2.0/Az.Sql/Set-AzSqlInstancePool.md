---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411128"
---
# <span data-ttu-id="0c32a-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="0c32a-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="0c32a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c32a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c32a-103">Anger egenskaper för en Azure SQL-instanskonstruktor.</span><span class="sxs-lookup"><span data-stu-id="0c32a-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="0c32a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c32a-104">SYNTAX</span></span>

### <span data-ttu-id="0c32a-105">DefaultSetInstancePoolParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0c32a-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c32a-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c32a-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c32a-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c32a-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c32a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c32a-108">DESCRIPTION</span></span>
<span data-ttu-id="0c32a-109">Cmdleten **set-AzSqlInstancePool** ändrar egenskaper för en Azure SQL-instanskonstruktor.</span><span class="sxs-lookup"><span data-stu-id="0c32a-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="0c32a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c32a-110">EXAMPLES</span></span>

### <span data-ttu-id="0c32a-111">Exempel 1: Ange licens typ för en instans av en pool</span><span class="sxs-lookup"><span data-stu-id="0c32a-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
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

<span data-ttu-id="0c32a-112">Det här kommandot anger licens typ och/eller taggar för en instans med namnet instancePool0.</span><span class="sxs-lookup"><span data-stu-id="0c32a-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="0c32a-113">Exempel 2: Ange en licens typ för en instans av en pool med ett instans objekt för poolen</span><span class="sxs-lookup"><span data-stu-id="0c32a-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
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

<span data-ttu-id="0c32a-114">Det här kommandot anger licens typen och/eller-taggar för en instans med ett instans objekt.</span><span class="sxs-lookup"><span data-stu-id="0c32a-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="0c32a-115">Exempel 3: Ange en licens typ för en instans av en pool med resurs-ID för en resurspool</span><span class="sxs-lookup"><span data-stu-id="0c32a-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
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

<span data-ttu-id="0c32a-116">Det här kommandot anger licens typ och/eller taggar för en instans med namnet instancePool0.</span><span class="sxs-lookup"><span data-stu-id="0c32a-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="0c32a-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c32a-117">PARAMETERS</span></span>

### <span data-ttu-id="0c32a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c32a-118">-AsJob</span></span>
<span data-ttu-id="0c32a-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0c32a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c32a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c32a-120">-DefaultProfile</span></span>
<span data-ttu-id="0c32a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c32a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c32a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c32a-122">-InputObject</span></span>
<span data-ttu-id="0c32a-123">Instansen för instance pool.</span><span class="sxs-lookup"><span data-stu-id="0c32a-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c32a-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0c32a-124">-LicenseType</span></span>
<span data-ttu-id="0c32a-125">Avgör vilken licens typ som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0c32a-125">Determines which License Type to use.</span></span>
<span data-ttu-id="0c32a-126">Möjliga värden är BasePrice (med AHB rabatt) och LicenseIncluded (utan AHB rabatt).</span><span class="sxs-lookup"><span data-stu-id="0c32a-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c32a-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c32a-127">-Name</span></span>
<span data-ttu-id="0c32a-128">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="0c32a-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c32a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c32a-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c32a-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0c32a-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c32a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c32a-131">-ResourceId</span></span>
<span data-ttu-id="0c32a-132">Resurs-ID för entitetsinstansen.</span><span class="sxs-lookup"><span data-stu-id="0c32a-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c32a-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0c32a-133">-Tag</span></span>
<span data-ttu-id="0c32a-134">Taggarna som ska kopplas till förekomsten</span><span class="sxs-lookup"><span data-stu-id="0c32a-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="0c32a-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0c32a-135">-Confirm</span></span>
<span data-ttu-id="0c32a-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c32a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c32a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c32a-137">-WhatIf</span></span>
<span data-ttu-id="0c32a-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0c32a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c32a-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0c32a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c32a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c32a-140">CommonParameters</span></span>
<span data-ttu-id="0c32a-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c32a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c32a-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c32a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c32a-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c32a-143">INPUTS</span></span>

### <span data-ttu-id="0c32a-144">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="0c32a-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="0c32a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0c32a-145">System.String</span></span>

## <span data-ttu-id="0c32a-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c32a-146">OUTPUTS</span></span>

### <span data-ttu-id="0c32a-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="0c32a-147">System.Object</span></span>
## <span data-ttu-id="0c32a-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c32a-148">NOTES</span></span>

## <span data-ttu-id="0c32a-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c32a-149">RELATED LINKS</span></span>
