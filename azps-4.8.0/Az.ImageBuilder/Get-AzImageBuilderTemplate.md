---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261099"
---
# <span data-ttu-id="dd9e5-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="dd9e5-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="dd9e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9e5-103">Hämta information om en mall för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="dd9e5-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="dd9e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd9e5-104">SYNTAX</span></span>

### <span data-ttu-id="dd9e5-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="dd9e5-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd9e5-106">Lära</span><span class="sxs-lookup"><span data-stu-id="dd9e5-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd9e5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd9e5-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd9e5-108">List1</span><span class="sxs-lookup"><span data-stu-id="dd9e5-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dd9e5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd9e5-109">DESCRIPTION</span></span>
<span data-ttu-id="dd9e5-110">Hämta information om en mall för virtuell dator</span><span class="sxs-lookup"><span data-stu-id="dd9e5-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="dd9e5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd9e5-111">EXAMPLES</span></span>

### <span data-ttu-id="dd9e5-112">Exempel 1: lista alla mallar under ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="dd9e5-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="dd9e5-113">Det här kommandot visar alla mallar under ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="dd9e5-114">Exempel 2: lista alla mallar under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="dd9e5-114">Example 2: List all template under a resource group</span></span>
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

<span data-ttu-id="dd9e5-115">Det här kommandot visar alla mallar under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="dd9e5-116">Exempel 3: Hämta en mall under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="dd9e5-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="dd9e5-117">Det här kommandot får en mall under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="dd9e5-118">Exempel 4: Hämta en mall under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="dd9e5-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="dd9e5-119">Det här kommandot får en mall under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="dd9e5-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd9e5-120">PARAMETERS</span></span>

### <span data-ttu-id="dd9e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9e5-121">-DefaultProfile</span></span>
<span data-ttu-id="dd9e5-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd9e5-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="dd9e5-123">-ImageTemplateName</span></span>
<span data-ttu-id="dd9e5-124">Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="dd9e5-124">The name of the image Template</span></span>

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

### <span data-ttu-id="dd9e5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd9e5-125">-InputObject</span></span>
<span data-ttu-id="dd9e5-126">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dd9e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd9e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd9e5-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd9e5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd9e5-129">-SubscriptionId</span></span>
<span data-ttu-id="dd9e5-130">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd9e5-131">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dd9e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9e5-132">CommonParameters</span></span>
<span data-ttu-id="dd9e5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd9e5-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd9e5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9e5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd9e5-135">INPUTS</span></span>

### <span data-ttu-id="dd9e5-136">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="dd9e5-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="dd9e5-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd9e5-137">OUTPUTS</span></span>

### <span data-ttu-id="dd9e5-138">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="dd9e5-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="dd9e5-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd9e5-139">NOTES</span></span>

<span data-ttu-id="dd9e5-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dd9e5-140">ALIASES</span></span>

<span data-ttu-id="dd9e5-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="dd9e5-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd9e5-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd9e5-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd9e5-144">INPUTOBJECT <IImageBuilderIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="dd9e5-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd9e5-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="dd9e5-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd9e5-146">`[ImageTemplateName <String>]`: Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="dd9e5-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="dd9e5-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="dd9e5-148">`[RunOutputName <String>]`: Namnet på Kör-resultatet</span><span class="sxs-lookup"><span data-stu-id="dd9e5-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="dd9e5-149">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dd9e5-150">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dd9e5-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dd9e5-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd9e5-151">RELATED LINKS</span></span>

