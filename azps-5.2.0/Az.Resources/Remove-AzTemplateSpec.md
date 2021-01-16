---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407664"
---
# <span data-ttu-id="cc2f3-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="cc2f3-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="cc2f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="cc2f3-103">Tar bort en mall-specifikation</span><span class="sxs-lookup"><span data-stu-id="cc2f3-103">Removes a Template Spec</span></span>

## <span data-ttu-id="cc2f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc2f3-104">SYNTAX</span></span>

### <span data-ttu-id="cc2f3-105">RemoveByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cc2f3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc2f3-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc2f3-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc2f3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc2f3-107">DESCRIPTION</span></span>
<span data-ttu-id="cc2f3-108">Tar bort en specifik mall. Om parametern version **-version** anges tas bara den angivna versionen bort.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="cc2f3-109">Om ingen specifik version anges tas mallens specifikationer och alla dess versioner bort.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="cc2f3-110">Om flaggan **-Force** finns tillgänglig visas ingen uppmaning om att ta bort den.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="cc2f3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc2f3-111">EXAMPLES</span></span>

### <span data-ttu-id="cc2f3-112">Exempel 1: ta bort en specifik version med namn</span><span class="sxs-lookup"><span data-stu-id="cc2f3-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="cc2f3-113">Tar bort version ' v 1.0 ' för mallnamnet "MyTemplateSpec" i resurs gruppen "myRG".</span><span class="sxs-lookup"><span data-stu-id="cc2f3-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="cc2f3-114">Exempel 2: ta bort en specifik version via resurs-ID</span><span class="sxs-lookup"><span data-stu-id="cc2f3-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="cc2f3-115">Tar bort version ' v 1.0 ' för mallnamnet med namnet "MyTemplateSpec" i resurs gruppen "myRG" för abonnemanget \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="cc2f3-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="cc2f3-116">Exempel 3: ta bort en specifikation och alla versioner efter namn</span><span class="sxs-lookup"><span data-stu-id="cc2f3-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="cc2f3-117">Tar bort den spec som heter ' MyTemplateSpec ' och alla dess versioner i resurs gruppen ' myRG '.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="cc2f3-118">Exempel 3: ta bort en specifikation och alla versioner efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="cc2f3-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="cc2f3-119">Tar bort den spec som heter ' MyTemplateSpec ' och alla dess versioner i resurs gruppen ' myRG ' för abonnemanget \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="cc2f3-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="cc2f3-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc2f3-120">PARAMETERS</span></span>

### <span data-ttu-id="cc2f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc2f3-121">-DefaultProfile</span></span>
<span data-ttu-id="cc2f3-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc2f3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cc2f3-123">-Force</span></span>
<span data-ttu-id="cc2f3-124">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cc2f3-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc2f3-125">-Name</span></span>
<span data-ttu-id="cc2f3-126">Namnet på mallens spec.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc2f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc2f3-128">Namnet på resurs gruppen för den här mallen.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2f3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc2f3-129">-ResourceId</span></span>
<span data-ttu-id="cc2f3-130">Fullständigt resurs-ID för mallens spec. exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="cc2f3-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2f3-131">-Version</span><span class="sxs-lookup"><span data-stu-id="cc2f3-131">-Version</span></span>
<span data-ttu-id="cc2f3-132">Den version av den mall som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc2f3-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc2f3-133">-Confirm</span></span>
<span data-ttu-id="cc2f3-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc2f3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc2f3-135">-WhatIf</span></span>
<span data-ttu-id="cc2f3-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc2f3-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc2f3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc2f3-138">CommonParameters</span></span>
<span data-ttu-id="cc2f3-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc2f3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc2f3-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc2f3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc2f3-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc2f3-141">INPUTS</span></span>

### <span data-ttu-id="cc2f3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cc2f3-142">System.String</span></span>

## <span data-ttu-id="cc2f3-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc2f3-143">OUTPUTS</span></span>

### <span data-ttu-id="cc2f3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc2f3-144">System.Boolean</span></span>

## <span data-ttu-id="cc2f3-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc2f3-145">NOTES</span></span>

## <span data-ttu-id="cc2f3-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc2f3-146">RELATED LINKS</span></span>
