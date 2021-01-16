---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426088"
---
# <span data-ttu-id="84daf-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="84daf-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="84daf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84daf-102">SYNOPSIS</span></span>
<span data-ttu-id="84daf-103">Skapa en mall för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="84daf-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="84daf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84daf-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84daf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84daf-105">DESCRIPTION</span></span>
<span data-ttu-id="84daf-106">Skapa en mall för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="84daf-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="84daf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84daf-107">EXAMPLES</span></span>

### <span data-ttu-id="84daf-108">Exempel 1: skapa en mall för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="84daf-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="84daf-109">Med de här kommandona skapar du en mall för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="84daf-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="84daf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84daf-110">PARAMETERS</span></span>

### <span data-ttu-id="84daf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84daf-111">-AsJob</span></span>
<span data-ttu-id="84daf-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="84daf-112">Run the command as a job</span></span>

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

### <span data-ttu-id="84daf-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="84daf-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="84daf-114">Maximal varaktighet att vänta medan bild mal len skapas.</span><span class="sxs-lookup"><span data-stu-id="84daf-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="84daf-115">Utelämna eller ange 0 för att använda standardvärdet (4 timmar).</span><span class="sxs-lookup"><span data-stu-id="84daf-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="84daf-116">-Anpassa</span><span class="sxs-lookup"><span data-stu-id="84daf-116">-Customize</span></span>
<span data-ttu-id="84daf-117">Anger egenskaperna som används för att beskriva anpassnings stegen i bilden, till exempel bild källa etc. Om du vill skapa läser du avsnittet anteckningar för anpassa egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="84daf-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84daf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84daf-118">-DefaultProfile</span></span>
<span data-ttu-id="84daf-119">regionen HideParameter autentiseringsuppgifterna, kontot, innehavaren och prenumerationen som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84daf-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84daf-120">-Distribuera</span><span class="sxs-lookup"><span data-stu-id="84daf-120">-Distribute</span></span>
<span data-ttu-id="84daf-121">De distributions mål där bild utskriften måste gå till.</span><span class="sxs-lookup"><span data-stu-id="84daf-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="84daf-122">Om du vill skapa läser du avsnittet anteckningar för distribuera egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="84daf-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84daf-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="84daf-123">-ImageTemplateName</span></span>
<span data-ttu-id="84daf-124">Namnet på bild mal len.</span><span class="sxs-lookup"><span data-stu-id="84daf-124">The name of the image Template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84daf-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="84daf-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="84daf-126">Slut tid för den senaste körningen (UTC).</span><span class="sxs-lookup"><span data-stu-id="84daf-126">End time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84daf-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="84daf-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="84daf-128">Utförlig information om det senaste körnings tillståndet.</span><span class="sxs-lookup"><span data-stu-id="84daf-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="84daf-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="84daf-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="84daf-130">Status för den senaste körningen.</span><span class="sxs-lookup"><span data-stu-id="84daf-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84daf-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="84daf-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="84daf-132">Under status för den senaste körningen.</span><span class="sxs-lookup"><span data-stu-id="84daf-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84daf-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="84daf-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="84daf-134">Start tid för den senaste körningen (UTC).</span><span class="sxs-lookup"><span data-stu-id="84daf-134">Start time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84daf-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="84daf-135">-Location</span></span>
<span data-ttu-id="84daf-136">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="84daf-136">Resource location.</span></span>

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

### <span data-ttu-id="84daf-137">-Nowait</span><span class="sxs-lookup"><span data-stu-id="84daf-137">-NoWait</span></span>
<span data-ttu-id="84daf-138">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="84daf-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84daf-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="84daf-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="84daf-140">Felkod för etableringen misslyckades.</span><span class="sxs-lookup"><span data-stu-id="84daf-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84daf-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="84daf-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="84daf-142">Utförligt fel meddelande om konfigurations fel.</span><span class="sxs-lookup"><span data-stu-id="84daf-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="84daf-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84daf-143">-ResourceGroupName</span></span>
<span data-ttu-id="84daf-144">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="84daf-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="84daf-145">-Källa</span><span class="sxs-lookup"><span data-stu-id="84daf-145">-Source</span></span>
<span data-ttu-id="84daf-146">Beskriver en virtuell dator bild källa för att bygga, anpassa och distribuera.</span><span class="sxs-lookup"><span data-stu-id="84daf-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="84daf-147">Om du vill skapa läser du avsnittet anteckningar för käll egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="84daf-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84daf-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84daf-148">-SubscriptionId</span></span>
<span data-ttu-id="84daf-149">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="84daf-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="84daf-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="84daf-150">-Tag</span></span>
<span data-ttu-id="84daf-151">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="84daf-151">Resource tags.</span></span>

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

### <span data-ttu-id="84daf-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="84daf-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="84daf-153">ID för användarens tilldelade identitet.</span><span class="sxs-lookup"><span data-stu-id="84daf-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="84daf-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="84daf-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="84daf-155">Storleken på OS-disken i GB.</span><span class="sxs-lookup"><span data-stu-id="84daf-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="84daf-156">Utelämna eller ange 0 för att använda Azures standard disk storlek.</span><span class="sxs-lookup"><span data-stu-id="84daf-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="84daf-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="84daf-157">-VMProfileVmSize</span></span>
<span data-ttu-id="84daf-158">Storleken på den virtuella datorn som används för att skapa, anpassa och avbilda bilder.</span><span class="sxs-lookup"><span data-stu-id="84daf-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="84daf-159">Utelämna eller ange en tom sträng om du vill använda standardvärdet (Standard_D1_v2).</span><span class="sxs-lookup"><span data-stu-id="84daf-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="84daf-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="84daf-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="84daf-161">Resurs-ID för ett redan befintligt undernät.</span><span class="sxs-lookup"><span data-stu-id="84daf-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="84daf-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84daf-162">-Confirm</span></span>
<span data-ttu-id="84daf-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84daf-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84daf-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84daf-164">-WhatIf</span></span>
<span data-ttu-id="84daf-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="84daf-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84daf-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="84daf-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84daf-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84daf-167">CommonParameters</span></span>
<span data-ttu-id="84daf-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84daf-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84daf-169">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84daf-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84daf-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84daf-170">INPUTS</span></span>

## <span data-ttu-id="84daf-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84daf-171">OUTPUTS</span></span>

### <span data-ttu-id="84daf-172">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="84daf-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="84daf-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84daf-173">NOTES</span></span>

<span data-ttu-id="84daf-174">ALIAS</span><span class="sxs-lookup"><span data-stu-id="84daf-174">ALIASES</span></span>

<span data-ttu-id="84daf-175">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="84daf-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="84daf-176">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="84daf-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84daf-177">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="84daf-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="84daf-178">ANPASSA <IImageTemplateCustomizer [] >: anger egenskaperna som används för att beskriva anpassnings stegen i bilden, till exempel bild källa etc.</span><span class="sxs-lookup"><span data-stu-id="84daf-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="84daf-179">`Type <String>`: Den typ av anpassnings verktyg som du vill använda på bilden.</span><span class="sxs-lookup"><span data-stu-id="84daf-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="84daf-180">"Shell" kan till exempel vara Shell-anpassning</span><span class="sxs-lookup"><span data-stu-id="84daf-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="84daf-181">`[Name <String>]`: Eget namn för att ange sammanhang för det här anpassade steget</span><span class="sxs-lookup"><span data-stu-id="84daf-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="84daf-182">DISTRIBUERA <IImageTemplateDistributor [] >: distributions målen där bild utskriften måste gå till.</span><span class="sxs-lookup"><span data-stu-id="84daf-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="84daf-183">`RunOutputName <String>`: Namnet som ska användas för den associerade RunOutput.</span><span class="sxs-lookup"><span data-stu-id="84daf-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="84daf-184">`Type <String>`: Typ av fördelning.</span><span class="sxs-lookup"><span data-stu-id="84daf-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="84daf-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Taggar som kommer att tillämpas på artefakten när den har skapats/uppdaterats av distributören.</span><span class="sxs-lookup"><span data-stu-id="84daf-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="84daf-186">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="84daf-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="84daf-187">KÄLLA <IImageTemplateSource> : beskriver en virtuell dator bild källa för att bygga, anpassa och distribuera.</span><span class="sxs-lookup"><span data-stu-id="84daf-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="84daf-188">`Type <String>`: Anger vilken typ av källbild du vill börja med.</span><span class="sxs-lookup"><span data-stu-id="84daf-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="84daf-189">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84daf-189">RELATED LINKS</span></span>

