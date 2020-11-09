---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323501"
---
# <span data-ttu-id="c1aad-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="c1aad-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="c1aad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1aad-102">SYNOPSIS</span></span>
<span data-ttu-id="c1aad-103">Skapa eller uppdatera ett privat moln</span><span class="sxs-lookup"><span data-stu-id="c1aad-103">Create or update a private cloud</span></span>

## <span data-ttu-id="c1aad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1aad-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1aad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1aad-105">DESCRIPTION</span></span>
<span data-ttu-id="c1aad-106">Skapa eller uppdatera ett privat moln</span><span class="sxs-lookup"><span data-stu-id="c1aad-106">Create or update a private cloud</span></span>

## <span data-ttu-id="c1aad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1aad-107">EXAMPLES</span></span>

### <span data-ttu-id="c1aad-108">Exempel 1: skapa ett privat moln</span><span class="sxs-lookup"><span data-stu-id="c1aad-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="c1aad-109">Skapa privat moln</span><span class="sxs-lookup"><span data-stu-id="c1aad-109">Create private cloud</span></span>

## <span data-ttu-id="c1aad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1aad-110">PARAMETERS</span></span>

### <span data-ttu-id="c1aad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1aad-111">-AsJob</span></span>
<span data-ttu-id="c1aad-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="c1aad-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c1aad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1aad-113">-DefaultProfile</span></span>
<span data-ttu-id="c1aad-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1aad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1aad-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="c1aad-115">-Internet</span></span>
<span data-ttu-id="c1aad-116">Anslutning till Internet är aktiverat eller inaktive rad</span><span class="sxs-lookup"><span data-stu-id="c1aad-116">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1aad-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="c1aad-117">-Location</span></span>
<span data-ttu-id="c1aad-118">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="c1aad-118">Resource location</span></span>

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

### <span data-ttu-id="c1aad-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="c1aad-119">-ManagementClusterSize</span></span>
<span data-ttu-id="c1aad-120">Kluster storlek</span><span class="sxs-lookup"><span data-stu-id="c1aad-120">The cluster size</span></span>

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

### <span data-ttu-id="c1aad-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="c1aad-121">-Name</span></span>
<span data-ttu-id="c1aad-122">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="c1aad-122">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1aad-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="c1aad-123">-NetworkBlock</span></span>
<span data-ttu-id="c1aad-124">Adress blocket ska vara unikt mellan VNet i ditt abonnemang och lokal.</span><span class="sxs-lookup"><span data-stu-id="c1aad-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="c1aad-125">Kontrol lera att CIDR-formatet är förenligt med (A. B. C. D/X) där A, B, C, D är mellan 0 och 255 och X är mellan 0 och 22</span><span class="sxs-lookup"><span data-stu-id="c1aad-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="c1aad-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c1aad-126">-NoWait</span></span>
<span data-ttu-id="c1aad-127">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="c1aad-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c1aad-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="c1aad-128">-NsxtPassword</span></span>
<span data-ttu-id="c1aad-129">Du kan också ange lösen ordet för NSX-T Manager när det privata molnet skapas</span><span class="sxs-lookup"><span data-stu-id="c1aad-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="c1aad-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1aad-130">-ResourceGroupName</span></span>
<span data-ttu-id="c1aad-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c1aad-131">The name of the resource group.</span></span>
<span data-ttu-id="c1aad-132">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="c1aad-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c1aad-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="c1aad-133">-Sku</span></span>
<span data-ttu-id="c1aad-134">Namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="c1aad-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="c1aad-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1aad-135">-SubscriptionId</span></span>
<span data-ttu-id="c1aad-136">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c1aad-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c1aad-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c1aad-137">-Tag</span></span>
<span data-ttu-id="c1aad-138">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="c1aad-138">Resource tags</span></span>

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

### <span data-ttu-id="c1aad-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="c1aad-139">-VcenterPassword</span></span>
<span data-ttu-id="c1aad-140">Du kan också ange lösen ordet för vCenter-administratörer när det privata molnet skapas</span><span class="sxs-lookup"><span data-stu-id="c1aad-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="c1aad-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1aad-141">-Confirm</span></span>
<span data-ttu-id="c1aad-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1aad-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1aad-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1aad-143">-WhatIf</span></span>
<span data-ttu-id="c1aad-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1aad-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1aad-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1aad-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1aad-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1aad-146">CommonParameters</span></span>
<span data-ttu-id="c1aad-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1aad-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1aad-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1aad-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1aad-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1aad-149">INPUTS</span></span>

## <span data-ttu-id="c1aad-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1aad-150">OUTPUTS</span></span>

### <span data-ttu-id="c1aad-151">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="c1aad-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="c1aad-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1aad-152">NOTES</span></span>

<span data-ttu-id="c1aad-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c1aad-153">ALIASES</span></span>

## <span data-ttu-id="c1aad-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1aad-154">RELATED LINKS</span></span>

