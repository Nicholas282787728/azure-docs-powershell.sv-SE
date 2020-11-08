---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWarePrivateCloud.md
ms.openlocfilehash: 5dd91db9a8141bf9992da9eb364b00301036a898
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261163"
---
# <span data-ttu-id="df7cc-101">New-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="df7cc-101">New-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="df7cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="df7cc-103">Skapa eller uppdatera ett privat moln</span><span class="sxs-lookup"><span data-stu-id="df7cc-103">Create or update a private cloud</span></span>

## <span data-ttu-id="df7cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df7cc-104">SYNTAX</span></span>

```
New-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> -Location <String>
 -ManagementClusterSize <Int32> -NetworkBlock <String> -Sku <String> [-SubscriptionId <String>]
 [-Internet <InternetEnum>] [-NsxtPassword <String>] [-Tag <Hashtable>] [-VcenterPassword <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df7cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df7cc-105">DESCRIPTION</span></span>
<span data-ttu-id="df7cc-106">Skapa eller uppdatera ett privat moln</span><span class="sxs-lookup"><span data-stu-id="df7cc-106">Create or update a private cloud</span></span>

## <span data-ttu-id="df7cc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df7cc-107">EXAMPLES</span></span>

### <span data-ttu-id="df7cc-108">Exempel 1: skapa ett privat moln</span><span class="sxs-lookup"><span data-stu-id="df7cc-108">Example 1: Create private cloud</span></span>
```powershell
PS C:\> New-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -NetworkBlock 192.168.48.0/22 -SkuName av36 -ManagementClusterSize 3 -Location australiaeast

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="df7cc-109">Skapa privat moln</span><span class="sxs-lookup"><span data-stu-id="df7cc-109">Create private cloud</span></span>

## <span data-ttu-id="df7cc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df7cc-110">PARAMETERS</span></span>

### <span data-ttu-id="df7cc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df7cc-111">-AsJob</span></span>
<span data-ttu-id="df7cc-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="df7cc-112">Run the command as a job</span></span>

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

### <span data-ttu-id="df7cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7cc-113">-DefaultProfile</span></span>
<span data-ttu-id="df7cc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df7cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df7cc-115">-Internet</span><span class="sxs-lookup"><span data-stu-id="df7cc-115">-Internet</span></span>
<span data-ttu-id="df7cc-116">Anslutning till Internet är aktiverat eller inaktive rad</span><span class="sxs-lookup"><span data-stu-id="df7cc-116">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="df7cc-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="df7cc-117">-Location</span></span>
<span data-ttu-id="df7cc-118">Resurs plats</span><span class="sxs-lookup"><span data-stu-id="df7cc-118">Resource location</span></span>

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

### <span data-ttu-id="df7cc-119">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="df7cc-119">-ManagementClusterSize</span></span>
<span data-ttu-id="df7cc-120">Kluster storlek</span><span class="sxs-lookup"><span data-stu-id="df7cc-120">The cluster size</span></span>

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

### <span data-ttu-id="df7cc-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="df7cc-121">-Name</span></span>
<span data-ttu-id="df7cc-122">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="df7cc-122">Name of the private cloud</span></span>

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

### <span data-ttu-id="df7cc-123">-NetworkBlock</span><span class="sxs-lookup"><span data-stu-id="df7cc-123">-NetworkBlock</span></span>
<span data-ttu-id="df7cc-124">Adress blocket ska vara unikt mellan VNet i ditt abonnemang och lokal.</span><span class="sxs-lookup"><span data-stu-id="df7cc-124">The block of addresses should be unique across VNet in your subscription as well as on-premise.</span></span>
<span data-ttu-id="df7cc-125">Kontrol lera att CIDR-formatet är förenligt med (A. B. C. D/X) där A, B, C, D är mellan 0 och 255 och X är mellan 0 och 22</span><span class="sxs-lookup"><span data-stu-id="df7cc-125">Make sure the CIDR format is conformed to (A.B.C.D/X) where A,B,C,D are between 0 and 255, and X is between 0 and 22</span></span>

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

### <span data-ttu-id="df7cc-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="df7cc-126">-NoWait</span></span>
<span data-ttu-id="df7cc-127">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="df7cc-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="df7cc-128">-NsxtPassword</span><span class="sxs-lookup"><span data-stu-id="df7cc-128">-NsxtPassword</span></span>
<span data-ttu-id="df7cc-129">Du kan också ange lösen ordet för NSX-T Manager när det privata molnet skapas</span><span class="sxs-lookup"><span data-stu-id="df7cc-129">Optionally, set the NSX-T Manager password when the private cloud is created</span></span>

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

### <span data-ttu-id="df7cc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7cc-130">-ResourceGroupName</span></span>
<span data-ttu-id="df7cc-131">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="df7cc-131">The name of the resource group.</span></span>
<span data-ttu-id="df7cc-132">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="df7cc-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="df7cc-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="df7cc-133">-Sku</span></span>
<span data-ttu-id="df7cc-134">Namnet på SKU: n.</span><span class="sxs-lookup"><span data-stu-id="df7cc-134">The name of the SKU.</span></span>

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

### <span data-ttu-id="df7cc-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df7cc-135">-SubscriptionId</span></span>
<span data-ttu-id="df7cc-136">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="df7cc-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="df7cc-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="df7cc-137">-Tag</span></span>
<span data-ttu-id="df7cc-138">Resursfiler</span><span class="sxs-lookup"><span data-stu-id="df7cc-138">Resource tags</span></span>

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

### <span data-ttu-id="df7cc-139">-VcenterPassword</span><span class="sxs-lookup"><span data-stu-id="df7cc-139">-VcenterPassword</span></span>
<span data-ttu-id="df7cc-140">Du kan också ange lösen ordet för vCenter-administratörer när det privata molnet skapas</span><span class="sxs-lookup"><span data-stu-id="df7cc-140">Optionally, set the vCenter admin password when the private cloud is created</span></span>

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

### <span data-ttu-id="df7cc-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df7cc-141">-Confirm</span></span>
<span data-ttu-id="df7cc-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df7cc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df7cc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df7cc-143">-WhatIf</span></span>
<span data-ttu-id="df7cc-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df7cc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df7cc-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df7cc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df7cc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7cc-146">CommonParameters</span></span>
<span data-ttu-id="df7cc-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7cc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7cc-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df7cc-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7cc-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df7cc-149">INPUTS</span></span>

## <span data-ttu-id="df7cc-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df7cc-150">OUTPUTS</span></span>

### <span data-ttu-id="df7cc-151">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="df7cc-151">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="df7cc-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df7cc-152">NOTES</span></span>

<span data-ttu-id="df7cc-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="df7cc-153">ALIASES</span></span>

## <span data-ttu-id="df7cc-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df7cc-154">RELATED LINKS</span></span>

