---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9c18597da52900794e5f891fb06385249c173a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088858"
---
# <span data-ttu-id="28017-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="28017-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="28017-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28017-102">SYNOPSIS</span></span>
<span data-ttu-id="28017-103">Skapar ett nytt Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="28017-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="28017-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28017-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28017-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28017-105">DESCRIPTION</span></span>
<span data-ttu-id="28017-106">Skapar ett nytt Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="28017-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="28017-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28017-107">EXAMPLES</span></span>

### <span data-ttu-id="28017-108">Exempel 1 – Skapa ett nytt Kusto-kluster</span><span class="sxs-lookup"><span data-stu-id="28017-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="28017-109">Med kommandot ovan skapas ett nytt Kusto-kluster med namnet "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="28017-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="28017-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28017-110">PARAMETERS</span></span>

### <span data-ttu-id="28017-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28017-111">-DefaultProfile</span></span>
<span data-ttu-id="28017-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28017-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28017-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="28017-113">-Location</span></span>
<span data-ttu-id="28017-114">Azure region där klustret ska skapas.</span><span class="sxs-lookup"><span data-stu-id="28017-114">Azure region where the cluster should be created.</span></span>

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

### <span data-ttu-id="28017-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="28017-115">-Name</span></span>
<span data-ttu-id="28017-116">Namn på det kluster som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="28017-116">Name of the cluster to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28017-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28017-117">-ResourceGroupName</span></span>
<span data-ttu-id="28017-118">Namnet på den resurs grupp under vilket du vill skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="28017-118">Name of resource group under which you want to create the cluster.</span></span>

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

### <span data-ttu-id="28017-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="28017-119">-Sku</span></span>
<span data-ttu-id="28017-120">Namn på SKU som används för att skapa klustret</span><span class="sxs-lookup"><span data-stu-id="28017-120">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="28017-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="28017-121">-Tag</span></span>
<span data-ttu-id="28017-122">En sträng, en sträng ord lista med flaggor associerade till det här klustret</span><span class="sxs-lookup"><span data-stu-id="28017-122">A string,string dictionary of tags associated with this cluster</span></span>

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

### <span data-ttu-id="28017-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="28017-123">-Tier</span></span>
<span data-ttu-id="28017-124">Namn på den nivå som används för att skapa klustret</span><span class="sxs-lookup"><span data-stu-id="28017-124">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="28017-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28017-125">-Confirm</span></span>
<span data-ttu-id="28017-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28017-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28017-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28017-127">-WhatIf</span></span>
<span data-ttu-id="28017-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28017-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28017-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28017-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28017-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28017-130">CommonParameters</span></span>
<span data-ttu-id="28017-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28017-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28017-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28017-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28017-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28017-133">INPUTS</span></span>

### <span data-ttu-id="28017-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="28017-134">None</span></span>

## <span data-ttu-id="28017-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28017-135">OUTPUTS</span></span>

### <span data-ttu-id="28017-136">Microsoft. Azure. commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="28017-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="28017-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28017-137">NOTES</span></span>

## <span data-ttu-id="28017-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28017-138">RELATED LINKS</span></span>
