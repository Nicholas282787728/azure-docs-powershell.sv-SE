---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319524"
---
# <span data-ttu-id="88ab0-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="88ab0-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="88ab0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="88ab0-103">Hämta angivet kör-utdata för den angivna bildmall-resursen</span><span class="sxs-lookup"><span data-stu-id="88ab0-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="88ab0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88ab0-104">SYNTAX</span></span>

### <span data-ttu-id="88ab0-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="88ab0-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="88ab0-106">Lära</span><span class="sxs-lookup"><span data-stu-id="88ab0-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="88ab0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="88ab0-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="88ab0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88ab0-108">DESCRIPTION</span></span>
<span data-ttu-id="88ab0-109">Hämta angivet kör-utdata för den angivna bildmall-resursen</span><span class="sxs-lookup"><span data-stu-id="88ab0-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="88ab0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88ab0-110">EXAMPLES</span></span>

### <span data-ttu-id="88ab0-111">Exempel 1: Visa alla resultat under en mall</span><span class="sxs-lookup"><span data-stu-id="88ab0-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="88ab0-112">Det här kommandot visar alla kör resultat under en mall.</span><span class="sxs-lookup"><span data-stu-id="88ab0-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="88ab0-113">Exempel 2: få ett kör-resultat under en mall</span><span class="sxs-lookup"><span data-stu-id="88ab0-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="88ab0-114">Det här kommandot får ett kör-resultat under en mall.</span><span class="sxs-lookup"><span data-stu-id="88ab0-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="88ab0-115">Exempel 3: få ett kör-resultat under en mall</span><span class="sxs-lookup"><span data-stu-id="88ab0-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="88ab0-116">Det här kommandot får ett kör-resultat under en mall.</span><span class="sxs-lookup"><span data-stu-id="88ab0-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="88ab0-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88ab0-117">PARAMETERS</span></span>

### <span data-ttu-id="88ab0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ab0-118">-DefaultProfile</span></span>
<span data-ttu-id="88ab0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88ab0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88ab0-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="88ab0-120">-ImageTemplateName</span></span>
<span data-ttu-id="88ab0-121">Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="88ab0-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ab0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88ab0-122">-InputObject</span></span>
<span data-ttu-id="88ab0-123">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="88ab0-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88ab0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ab0-124">-ResourceGroupName</span></span>
<span data-ttu-id="88ab0-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88ab0-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ab0-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="88ab0-126">-RunOutputName</span></span>
<span data-ttu-id="88ab0-127">Namnet på Kör-resultatet</span><span class="sxs-lookup"><span data-stu-id="88ab0-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ab0-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88ab0-128">-SubscriptionId</span></span>
<span data-ttu-id="88ab0-129">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="88ab0-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="88ab0-130">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="88ab0-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ab0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ab0-131">CommonParameters</span></span>
<span data-ttu-id="88ab0-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ab0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ab0-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88ab0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ab0-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88ab0-134">INPUTS</span></span>

### <span data-ttu-id="88ab0-135">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="88ab0-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="88ab0-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88ab0-136">OUTPUTS</span></span>

### <span data-ttu-id="88ab0-137">Microsoft. Azure. PowerShell. cmdletar. ImageBuilder. Models. Api20200214. IRunOutput</span><span class="sxs-lookup"><span data-stu-id="88ab0-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="88ab0-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88ab0-138">NOTES</span></span>

<span data-ttu-id="88ab0-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="88ab0-139">ALIASES</span></span>

<span data-ttu-id="88ab0-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="88ab0-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88ab0-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="88ab0-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88ab0-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88ab0-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88ab0-143">INPUTOBJECT <IImageBuilderIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="88ab0-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88ab0-144">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="88ab0-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88ab0-145">`[ImageTemplateName <String>]`: Namnet på bild mal len</span><span class="sxs-lookup"><span data-stu-id="88ab0-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="88ab0-146">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="88ab0-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="88ab0-147">`[RunOutputName <String>]`: Namnet på Kör-resultatet</span><span class="sxs-lookup"><span data-stu-id="88ab0-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="88ab0-148">`[SubscriptionId <String>]`: Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="88ab0-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="88ab0-149">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="88ab0-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="88ab0-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88ab0-150">RELATED LINKS</span></span>
