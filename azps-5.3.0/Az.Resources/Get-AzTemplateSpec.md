---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521476"
---
# <span data-ttu-id="bcf91-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="bcf91-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="bcf91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bcf91-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf91-103">Hämtar eller visar mallens specifikationer</span><span class="sxs-lookup"><span data-stu-id="bcf91-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="bcf91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bcf91-104">SYNTAX</span></span>

### <span data-ttu-id="bcf91-105">ListTemplateSpecsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bcf91-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcf91-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf91-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcf91-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf91-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcf91-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bcf91-108">DESCRIPTION</span></span>
<span data-ttu-id="bcf91-109">Denna cmdlet kan användas för att ange listmallar i en prenumeration/resurs grupp eller för att få en specifik mall med namn eller ID. När du får en specifik mall genom att ange namn/ID för en specifik version kan du välja att hämta ett versions namn via parametern **-version** .</span><span class="sxs-lookup"><span data-stu-id="bcf91-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="bcf91-110">När **-version** används visas bara den specifika versions informationen i \**. Versioner* av spec-objektet för den returnerade mallen.</span><span class="sxs-lookup"><span data-stu-id="bcf91-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="bcf91-111">Om du inte har angett någon specifik version när du hämtar en mall specifikation via namn/ID finns alla versioner i \**. Egenskapen versions* för det returnerade objektet.</span><span class="sxs-lookup"><span data-stu-id="bcf91-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="bcf91-112">**Obs!** när du visar en lista med alla specifikationer för mallar i en prenumeration eller resurs grupp visas en specifikation för varje mall som returnerar *". Versions* värden är *Null*.</span><span class="sxs-lookup"><span data-stu-id="bcf91-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="bcf91-113">Versions information ingår endast när-namn-eller-ResourceId-parametrar tillhandahålls (tex: du begär en specifik mall specifikation/version).</span><span class="sxs-lookup"><span data-stu-id="bcf91-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="bcf91-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bcf91-114">EXAMPLES</span></span>

### <span data-ttu-id="bcf91-115">Exempel 1: specifikationer för listmall i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="bcf91-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="bcf91-116">Här listas alla specifikationer för mallar i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="bcf91-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="bcf91-117">Exempel 2: specifikationer för listmall i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="bcf91-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="bcf91-118">Visar alla mallalternativ i resurs gruppen ' myRG ' för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="bcf91-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="bcf91-119">Exempel 3: Hämta mall-specifikation (med alla versioner) efter namn</span><span class="sxs-lookup"><span data-stu-id="bcf91-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="bcf91-120">Hämtar information om mallnamnet "MyTemplateSpec" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="bcf91-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="bcf91-121">**Obs!** alla specifikationer för mallar finns i "*. Versioner*"-egenskapen för returvärdet.</span><span class="sxs-lookup"><span data-stu-id="bcf91-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="bcf91-122">Exempel 4: Hämta specifikation (specifik version) efter namn</span><span class="sxs-lookup"><span data-stu-id="bcf91-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="bcf91-123">Hämtar information om version ' v 1.0 ' för mallnamnet med namnet "MyTemplateSpec" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="bcf91-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="bcf91-124">**Obs!** *". Versioner "* egenskapen för det returnerade objektet innehåller endast den begärda versionen.</span><span class="sxs-lookup"><span data-stu-id="bcf91-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="bcf91-125">Exempel 5: Hämta mall-specifikation (med alla versioner) efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="bcf91-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="bcf91-126">Hämtar information om mallnamnet "MyTemplateSpec" i resurs gruppen "myRG" för prenumerations \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="bcf91-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="bcf91-127">**Obs!** alla specifikationer för mallar finns i "*. Versioner*"-egenskapen för returvärdet.</span><span class="sxs-lookup"><span data-stu-id="bcf91-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="bcf91-128">Exempel 6: Hämta mallens spec (specifik version) efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="bcf91-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="bcf91-129">Hämtar information om version ' v 1.0 ' för mallnamnet med namnet "MyTemplateSpec" i resurs gruppen "myRG" för abonnemanget \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="bcf91-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="bcf91-130">**Obs!** *". Versioner "* egenskapen för det returnerade objektet innehåller endast den begärda versionen.</span><span class="sxs-lookup"><span data-stu-id="bcf91-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="bcf91-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bcf91-131">PARAMETERS</span></span>

### <span data-ttu-id="bcf91-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf91-132">-DefaultProfile</span></span>
<span data-ttu-id="bcf91-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf91-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcf91-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="bcf91-134">-Name</span></span>
<span data-ttu-id="bcf91-135">Namnet på mallens spec.</span><span class="sxs-lookup"><span data-stu-id="bcf91-135">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf91-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf91-136">-ResourceGroupName</span></span>
<span data-ttu-id="bcf91-137">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bcf91-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf91-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf91-138">-ResourceId</span></span>
<span data-ttu-id="bcf91-139">Fullständigt resurs-ID för mallens spec. exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="bcf91-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf91-140">-Version</span><span class="sxs-lookup"><span data-stu-id="bcf91-140">-Version</span></span>
<span data-ttu-id="bcf91-141">Versionen av mallens spec.</span><span class="sxs-lookup"><span data-stu-id="bcf91-141">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf91-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf91-142">CommonParameters</span></span>
<span data-ttu-id="bcf91-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf91-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf91-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcf91-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf91-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bcf91-145">INPUTS</span></span>

### <span data-ttu-id="bcf91-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bcf91-146">System.String</span></span>

## <span data-ttu-id="bcf91-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bcf91-147">OUTPUTS</span></span>

### <span data-ttu-id="bcf91-148">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="bcf91-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="bcf91-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bcf91-149">NOTES</span></span>

## <span data-ttu-id="bcf91-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bcf91-150">RELATED LINKS</span></span>
