---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260190"
---
# <span data-ttu-id="5e2d7-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="5e2d7-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="5e2d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e2d7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e2d7-103">Skapa eller uppdatera ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="5e2d7-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="5e2d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e2d7-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e2d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e2d7-105">DESCRIPTION</span></span>
<span data-ttu-id="5e2d7-106">Skapa eller uppdatera ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="5e2d7-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="5e2d7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e2d7-107">EXAMPLES</span></span>

### <span data-ttu-id="5e2d7-108">Exempel 1: skapa kluster</span><span class="sxs-lookup"><span data-stu-id="5e2d7-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="5e2d7-109">Skapa kluster</span><span class="sxs-lookup"><span data-stu-id="5e2d7-109">Create cluster</span></span>

## <span data-ttu-id="5e2d7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e2d7-110">PARAMETERS</span></span>

### <span data-ttu-id="5e2d7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e2d7-111">-AsJob</span></span>
<span data-ttu-id="5e2d7-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="5e2d7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5e2d7-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="5e2d7-113">-ClusterSize</span></span>
<span data-ttu-id="5e2d7-114">Kluster storlek</span><span class="sxs-lookup"><span data-stu-id="5e2d7-114">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e2d7-115">-DefaultProfile</span></span>
<span data-ttu-id="5e2d7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5e2d7-117">-Name</span></span>
<span data-ttu-id="5e2d7-118">Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="5e2d7-118">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d7-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5e2d7-119">-NoWait</span></span>
<span data-ttu-id="5e2d7-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="5e2d7-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e2d7-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="5e2d7-121">-PrivateCloudName</span></span>
<span data-ttu-id="5e2d7-122">Namnet på det privata molnet.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="5e2d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e2d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e2d7-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-124">The name of the resource group.</span></span>
<span data-ttu-id="5e2d7-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5e2d7-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5e2d7-126">-SkuName</span></span>
<span data-ttu-id="5e2d7-127">Namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="5e2d7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e2d7-128">-SubscriptionId</span></span>
<span data-ttu-id="5e2d7-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2d7-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e2d7-130">-Confirm</span></span>
<span data-ttu-id="5e2d7-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e2d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e2d7-132">-WhatIf</span></span>
<span data-ttu-id="5e2d7-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e2d7-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e2d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e2d7-135">CommonParameters</span></span>
<span data-ttu-id="5e2d7-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e2d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e2d7-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e2d7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e2d7-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e2d7-138">INPUTS</span></span>

## <span data-ttu-id="5e2d7-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e2d7-139">OUTPUTS</span></span>

### <span data-ttu-id="5e2d7-140">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="5e2d7-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="5e2d7-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e2d7-141">NOTES</span></span>

<span data-ttu-id="5e2d7-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5e2d7-142">ALIASES</span></span>

## <span data-ttu-id="5e2d7-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e2d7-143">RELATED LINKS</span></span>

