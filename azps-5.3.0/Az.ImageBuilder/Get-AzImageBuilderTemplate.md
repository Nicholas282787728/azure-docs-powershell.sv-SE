---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523552"
---
# <span data-ttu-id="c46cf-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="c46cf-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="c46cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c46cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c46cf-103">Hämta information om en mall för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="c46cf-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="c46cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c46cf-104">SYNTAX</span></span>

### <span data-ttu-id="c46cf-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="c46cf-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c46cf-106">Lära</span><span class="sxs-lookup"><span data-stu-id="c46cf-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c46cf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c46cf-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c46cf-108">List1</span><span class="sxs-lookup"><span data-stu-id="c46cf-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c46cf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c46cf-109">DESCRIPTION</span></span>
<span data-ttu-id="c46cf-110">Hämta information om en mall för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="c46cf-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="c46cf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c46cf-111">EXAMPLES</span></span>

### <span data-ttu-id="c46cf-112">Exempel 1: lista alla mallar under ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="c46cf-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="c46cf-113">Det här kommandot visar alla mallar under ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c46cf-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="c46cf-114">Exempel 2: lista alla mallar under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c46cf-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="c46cf-115">Det här kommandot visar alla mallar under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c46cf-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="c46cf-116">Exempel 3: Hämta en mall under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c46cf-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="c46cf-117">Det här kommandot får en mall under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c46cf-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="c46cf-118">Exempel 4: Hämta en mall under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c46cf-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="c46cf-119">Det här kommandot får en mall under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c46cf-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="c46cf-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c46cf-120">PARAMETERS</span></span>

### <span data-ttu-id="c46cf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46cf-121">-DefaultProfile</span></span>
<span data-ttu-id="c46cf-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c46cf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c46cf-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="c46cf-123">-ImageTemplateName</span></span>
<span data-ttu-id="c46cf-124">Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="c46cf-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46cf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c46cf-125">-InputObject</span></span>
<span data-ttu-id="c46cf-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c46cf-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c46cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="c46cf-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c46cf-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46cf-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c46cf-129">-SubscriptionId</span></span>
<span data-ttu-id="c46cf-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c46cf-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c46cf-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c46cf-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46cf-132">CommonParameters</span></span>
<span data-ttu-id="c46cf-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c46cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46cf-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c46cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46cf-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c46cf-135">INPUTS</span></span>

### <span data-ttu-id="c46cf-136">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="c46cf-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="c46cf-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c46cf-137">OUTPUTS</span></span>

### <span data-ttu-id="c46cf-138">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="c46cf-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="c46cf-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c46cf-139">NOTES</span></span>

<span data-ttu-id="c46cf-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c46cf-140">ALIASES</span></span>

<span data-ttu-id="c46cf-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c46cf-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c46cf-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c46cf-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c46cf-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c46cf-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c46cf-144">INPUTOBJECT <IImageBuilderIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c46cf-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c46cf-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c46cf-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c46cf-146">`[ImageTemplateName <String>]`: Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="c46cf-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="c46cf-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c46cf-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c46cf-148">`[RunOutputName <String>]`: Namnet på Kör-resultatet</span><span class="sxs-lookup"><span data-stu-id="c46cf-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="c46cf-149">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c46cf-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c46cf-150">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="c46cf-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c46cf-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c46cf-151">RELATED LINKS</span></span>

