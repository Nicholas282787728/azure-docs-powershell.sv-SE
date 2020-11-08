---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 0b5e066255a0757c7aaafb6aee6c4ca37d03c7fa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088843"
---
# <span data-ttu-id="fedb8-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="fedb8-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="fedb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fedb8-102">SYNOPSIS</span></span>
<span data-ttu-id="fedb8-103">Uppdatera ett befintligt Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="fedb8-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="fedb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fedb8-104">SYNTAX</span></span>

### <span data-ttu-id="fedb8-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="fedb8-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fedb8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fedb8-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fedb8-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fedb8-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fedb8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fedb8-108">DESCRIPTION</span></span>
<span data-ttu-id="fedb8-109">Uppdatera ett befintligt Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="fedb8-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="fedb8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fedb8-110">EXAMPLES</span></span>

### <span data-ttu-id="fedb8-111">Exempel 1 – uppdatera ett befintligt kluster med namn</span><span class="sxs-lookup"><span data-stu-id="fedb8-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="fedb8-112">Kommandot ovan uppdaterar nivån för det Kusto klustret "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="fedb8-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="fedb8-113">Exempel 2 – uppdatera ett befintligt kluster med ledning</span><span class="sxs-lookup"><span data-stu-id="fedb8-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="fedb8-114">Kommandot ovan får Kusto-klustret "mykustocluster" i resurs gruppen "testrg" med hjälp av `Get-AzKustoCluster` cmdleten och sedan flyttas resultatet till `Update-AzKustoCluster` för att uppdatera klustrets nivå till "standard".</span><span class="sxs-lookup"><span data-stu-id="fedb8-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="fedb8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fedb8-115">PARAMETERS</span></span>

### <span data-ttu-id="fedb8-116">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="fedb8-116">-Capacity</span></span>
<span data-ttu-id="fedb8-117">Instans numret för VM.</span><span class="sxs-lookup"><span data-stu-id="fedb8-117">The instance number of the VM.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fedb8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fedb8-118">-DefaultProfile</span></span>
<span data-ttu-id="fedb8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fedb8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fedb8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fedb8-120">-InputObject</span></span>
<span data-ttu-id="fedb8-121">Kusto.</span><span class="sxs-lookup"><span data-stu-id="fedb8-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fedb8-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="fedb8-122">-Name</span></span>
<span data-ttu-id="fedb8-123">Namn på klustret som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="fedb8-123">Name of cluster to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fedb8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fedb8-124">-ResourceGroupName</span></span>
<span data-ttu-id="fedb8-125">Namnet på den resurs grupp som klustret finns under.</span><span class="sxs-lookup"><span data-stu-id="fedb8-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fedb8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fedb8-126">-ResourceId</span></span>
<span data-ttu-id="fedb8-127">Kusto-kluster-ResourceID.</span><span class="sxs-lookup"><span data-stu-id="fedb8-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedb8-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fedb8-128">-SkuName</span></span>
<span data-ttu-id="fedb8-129">Namn på SKU som används för att skapa klustret</span><span class="sxs-lookup"><span data-stu-id="fedb8-129">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="fedb8-130">-Tier</span><span class="sxs-lookup"><span data-stu-id="fedb8-130">-Tier</span></span>
<span data-ttu-id="fedb8-131">Namn på den nivå som används för att skapa klustret</span><span class="sxs-lookup"><span data-stu-id="fedb8-131">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="fedb8-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fedb8-132">-Confirm</span></span>
<span data-ttu-id="fedb8-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fedb8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fedb8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fedb8-134">-WhatIf</span></span>
<span data-ttu-id="fedb8-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fedb8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fedb8-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fedb8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fedb8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fedb8-137">CommonParameters</span></span>
<span data-ttu-id="fedb8-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fedb8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fedb8-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fedb8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fedb8-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fedb8-140">INPUTS</span></span>

### <span data-ttu-id="fedb8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fedb8-141">System.String</span></span>

### <span data-ttu-id="fedb8-142">Microsoft. Azure. commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="fedb8-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="fedb8-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fedb8-143">OUTPUTS</span></span>

### <span data-ttu-id="fedb8-144">Microsoft. Azure. commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="fedb8-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="fedb8-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fedb8-145">NOTES</span></span>

## <span data-ttu-id="fedb8-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fedb8-146">RELATED LINKS</span></span>