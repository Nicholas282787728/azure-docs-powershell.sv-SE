---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: d1da0ce7f8a88a12b0714960a60d5b2aa523a0a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920043"
---
# <span data-ttu-id="94028-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="94028-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="94028-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94028-102">SYNOPSIS</span></span>
<span data-ttu-id="94028-103">Definition av hanterade program uppdateringar</span><span class="sxs-lookup"><span data-stu-id="94028-103">Updates managed application definition</span></span>

## <span data-ttu-id="94028-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94028-104">SYNTAX</span></span>

### <span data-ttu-id="94028-105">SetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="94028-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94028-106">SetById</span><span class="sxs-lookup"><span data-stu-id="94028-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94028-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94028-107">DESCRIPTION</span></span>
<span data-ttu-id="94028-108">Cmdleten **set-AzManagedApplicationDefinition-** hanterade program definitioner</span><span class="sxs-lookup"><span data-stu-id="94028-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="94028-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94028-109">EXAMPLES</span></span>

### <span data-ttu-id="94028-110">Exempel 1: definitions beskrivning för uppdatera hanterade program</span><span class="sxs-lookup"><span data-stu-id="94028-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="94028-111">Det här kommandot uppdaterar definitionen för definition av hanterade program</span><span class="sxs-lookup"><span data-stu-id="94028-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="94028-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94028-112">PARAMETERS</span></span>

### <span data-ttu-id="94028-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="94028-113">-ApiVersion</span></span>
<span data-ttu-id="94028-114">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="94028-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="94028-115">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="94028-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="94028-116">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="94028-116">-Authorization</span></span>
<span data-ttu-id="94028-117">Tillstånd för hanterade program definitioner.</span><span class="sxs-lookup"><span data-stu-id="94028-117">The managed application definition authorization.</span></span>
<span data-ttu-id="94028-118">Semikolonavgränsade par i ett format med \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="94028-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94028-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94028-119">-DefaultProfile</span></span>
<span data-ttu-id="94028-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94028-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94028-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="94028-121">-Description</span></span>
<span data-ttu-id="94028-122">Definitions beskrivning för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="94028-122">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94028-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="94028-123">-DisplayName</span></span>
<span data-ttu-id="94028-124">Det hanterade visnings namnet för program definitionen.</span><span class="sxs-lookup"><span data-stu-id="94028-124">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94028-125">-ID</span><span class="sxs-lookup"><span data-stu-id="94028-125">-Id</span></span>
<span data-ttu-id="94028-126">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="94028-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="94028-127">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94028-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94028-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="94028-128">-Name</span></span>
<span data-ttu-id="94028-129">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="94028-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94028-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="94028-130">-PackageFileUri</span></span>
<span data-ttu-id="94028-131">Fil-URI för det hanterade programpaketet.</span><span class="sxs-lookup"><span data-stu-id="94028-131">The managed application definition package file uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94028-132">-För</span><span class="sxs-lookup"><span data-stu-id="94028-132">-Pre</span></span>
<span data-ttu-id="94028-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="94028-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="94028-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94028-134">-ResourceGroupName</span></span>
<span data-ttu-id="94028-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="94028-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94028-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="94028-136">-Tag</span></span>
<span data-ttu-id="94028-137">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="94028-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94028-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94028-138">-Confirm</span></span>
<span data-ttu-id="94028-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94028-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94028-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94028-140">-WhatIf</span></span>
<span data-ttu-id="94028-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94028-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94028-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94028-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94028-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94028-143">CommonParameters</span></span>
<span data-ttu-id="94028-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94028-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94028-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94028-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94028-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94028-146">INPUTS</span></span>

### <span data-ttu-id="94028-147">System. String</span><span class="sxs-lookup"><span data-stu-id="94028-147">System.String</span></span>

### <span data-ttu-id="94028-148">System. string []</span><span class="sxs-lookup"><span data-stu-id="94028-148">System.String[]</span></span>

### <span data-ttu-id="94028-149">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="94028-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="94028-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94028-150">OUTPUTS</span></span>

### <span data-ttu-id="94028-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="94028-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="94028-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94028-152">NOTES</span></span>

## <span data-ttu-id="94028-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94028-153">RELATED LINKS</span></span>
