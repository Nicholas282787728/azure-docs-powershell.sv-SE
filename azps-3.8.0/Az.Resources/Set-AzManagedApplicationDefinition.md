---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: aa9f743e8500450245bed96305138f4bf6e25c56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089465"
---
# <span data-ttu-id="07d7c-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="07d7c-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="07d7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="07d7c-103">Definition av hanterade program uppdateringar</span><span class="sxs-lookup"><span data-stu-id="07d7c-103">Updates managed application definition</span></span>

## <span data-ttu-id="07d7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07d7c-104">SYNTAX</span></span>

### <span data-ttu-id="07d7c-105">SetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="07d7c-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07d7c-106">SetById</span><span class="sxs-lookup"><span data-stu-id="07d7c-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07d7c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07d7c-107">DESCRIPTION</span></span>
<span data-ttu-id="07d7c-108">Cmdleten **set-AzManagedApplicationDefinition-** hanterade program definitioner</span><span class="sxs-lookup"><span data-stu-id="07d7c-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="07d7c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07d7c-109">EXAMPLES</span></span>

### <span data-ttu-id="07d7c-110">Exempel 1: definitions beskrivning för uppdatera hanterade program</span><span class="sxs-lookup"><span data-stu-id="07d7c-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="07d7c-111">Det här kommandot uppdaterar definitionen för definition av hanterade program</span><span class="sxs-lookup"><span data-stu-id="07d7c-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="07d7c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07d7c-112">PARAMETERS</span></span>

### <span data-ttu-id="07d7c-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="07d7c-113">-ApiVersion</span></span>
<span data-ttu-id="07d7c-114">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="07d7c-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="07d7c-115">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="07d7c-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="07d7c-116">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="07d7c-116">-Authorization</span></span>
<span data-ttu-id="07d7c-117">Tillstånd för hanterade program definitioner.</span><span class="sxs-lookup"><span data-stu-id="07d7c-117">The managed application definition authorization.</span></span>
<span data-ttu-id="07d7c-118">Semikolonavgränsade par i ett format med \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="07d7c-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="07d7c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07d7c-119">-DefaultProfile</span></span>
<span data-ttu-id="07d7c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07d7c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07d7c-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="07d7c-121">-Description</span></span>
<span data-ttu-id="07d7c-122">Definitions beskrivning för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="07d7c-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="07d7c-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="07d7c-123">-DisplayName</span></span>
<span data-ttu-id="07d7c-124">Det hanterade visnings namnet för program definitionen.</span><span class="sxs-lookup"><span data-stu-id="07d7c-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="07d7c-125">-ID</span><span class="sxs-lookup"><span data-stu-id="07d7c-125">-Id</span></span>
<span data-ttu-id="07d7c-126">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="07d7c-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="07d7c-127">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d7c-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="07d7c-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="07d7c-128">-Name</span></span>
<span data-ttu-id="07d7c-129">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="07d7c-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="07d7c-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="07d7c-130">-PackageFileUri</span></span>
<span data-ttu-id="07d7c-131">Fil-URI för det hanterade programpaketet.</span><span class="sxs-lookup"><span data-stu-id="07d7c-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="07d7c-132">-För</span><span class="sxs-lookup"><span data-stu-id="07d7c-132">-Pre</span></span>
<span data-ttu-id="07d7c-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="07d7c-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="07d7c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07d7c-134">-ResourceGroupName</span></span>
<span data-ttu-id="07d7c-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="07d7c-135">The resource group name.</span></span>

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

### <span data-ttu-id="07d7c-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="07d7c-136">-Tag</span></span>
<span data-ttu-id="07d7c-137">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="07d7c-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="07d7c-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07d7c-138">-Confirm</span></span>
<span data-ttu-id="07d7c-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07d7c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07d7c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07d7c-140">-WhatIf</span></span>
<span data-ttu-id="07d7c-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07d7c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07d7c-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07d7c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07d7c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d7c-143">CommonParameters</span></span>
<span data-ttu-id="07d7c-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07d7c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d7c-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07d7c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d7c-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07d7c-146">INPUTS</span></span>

### <span data-ttu-id="07d7c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="07d7c-147">System.String</span></span>

### <span data-ttu-id="07d7c-148">System. string []</span><span class="sxs-lookup"><span data-stu-id="07d7c-148">System.String[]</span></span>

### <span data-ttu-id="07d7c-149">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="07d7c-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="07d7c-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07d7c-150">OUTPUTS</span></span>

### <span data-ttu-id="07d7c-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="07d7c-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="07d7c-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07d7c-152">NOTES</span></span>

## <span data-ttu-id="07d7c-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07d7c-153">RELATED LINKS</span></span>
