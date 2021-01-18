---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareCluster.md
ms.openlocfilehash: f2ed1813859f92624696eef7fa4f881f3eba1628
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522153"
---
# <span data-ttu-id="f7e0f-101">New-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="f7e0f-101">New-AzVMWareCluster</span></span>

## <span data-ttu-id="f7e0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e0f-103">Skapa eller uppdatera ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="f7e0f-103">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="f7e0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7e0f-104">SYNTAX</span></span>

```
New-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String> -ClusterSize <Int32>
 -SkuName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f7e0f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7e0f-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e0f-106">Skapa eller uppdatera ett kluster i ett privat moln</span><span class="sxs-lookup"><span data-stu-id="f7e0f-106">Create or update a cluster in a private cloud</span></span>

## <span data-ttu-id="f7e0f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7e0f-107">EXAMPLES</span></span>

### <span data-ttu-id="f7e0f-108">Exempel 1: skapa kluster</span><span class="sxs-lookup"><span data-stu-id="f7e0f-108">Example 1: Create cluster</span></span>
```powershell
PS C:\> New-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group -ClusterSize 3 -SkuName av36

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="f7e0f-109">Skapa kluster</span><span class="sxs-lookup"><span data-stu-id="f7e0f-109">Create cluster</span></span>

## <span data-ttu-id="f7e0f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7e0f-110">PARAMETERS</span></span>

### <span data-ttu-id="f7e0f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7e0f-111">-AsJob</span></span>
<span data-ttu-id="f7e0f-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="f7e0f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f7e0f-113">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="f7e0f-113">-ClusterSize</span></span>
<span data-ttu-id="f7e0f-114">Kluster storlek</span><span class="sxs-lookup"><span data-stu-id="f7e0f-114">The cluster size</span></span>

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

### <span data-ttu-id="f7e0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e0f-115">-DefaultProfile</span></span>
<span data-ttu-id="f7e0f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7e0f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7e0f-117">-Name</span></span>
<span data-ttu-id="f7e0f-118">Namnet på klustret i det privata molnet</span><span class="sxs-lookup"><span data-stu-id="f7e0f-118">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="f7e0f-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f7e0f-119">-NoWait</span></span>
<span data-ttu-id="f7e0f-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="f7e0f-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f7e0f-121">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="f7e0f-121">-PrivateCloudName</span></span>
<span data-ttu-id="f7e0f-122">Namnet på det privata molnet.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-122">The name of the private cloud.</span></span>

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

### <span data-ttu-id="f7e0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7e0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7e0f-124">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-124">The name of the resource group.</span></span>
<span data-ttu-id="f7e0f-125">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f7e0f-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f7e0f-126">-SkuName</span></span>
<span data-ttu-id="f7e0f-127">Namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-127">The name of the SKU.</span></span>

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

### <span data-ttu-id="f7e0f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7e0f-128">-SubscriptionId</span></span>
<span data-ttu-id="f7e0f-129">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f7e0f-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7e0f-130">-Confirm</span></span>
<span data-ttu-id="f7e0f-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7e0f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e0f-132">-WhatIf</span></span>
<span data-ttu-id="f7e0f-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7e0f-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7e0f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e0f-135">CommonParameters</span></span>
<span data-ttu-id="f7e0f-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7e0f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e0f-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7e0f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e0f-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7e0f-138">INPUTS</span></span>

## <span data-ttu-id="f7e0f-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7e0f-139">OUTPUTS</span></span>

### <span data-ttu-id="f7e0f-140">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. ICluster</span><span class="sxs-lookup"><span data-stu-id="f7e0f-140">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="f7e0f-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7e0f-141">NOTES</span></span>

<span data-ttu-id="f7e0f-142">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f7e0f-142">ALIASES</span></span>

## <span data-ttu-id="f7e0f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7e0f-143">RELATED LINKS</span></span>

