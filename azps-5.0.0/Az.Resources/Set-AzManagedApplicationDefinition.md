---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: 3f7ee823441910e1e5e79da3901d4114f04fdd67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322818"
---
# <span data-ttu-id="5ee8b-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="5ee8b-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="5ee8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ee8b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee8b-103">Definition av hanterade program uppdateringar</span><span class="sxs-lookup"><span data-stu-id="5ee8b-103">Updates managed application definition</span></span>

## <span data-ttu-id="5ee8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ee8b-104">SYNTAX</span></span>

### <span data-ttu-id="5ee8b-105">SetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="5ee8b-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ee8b-106">SetById</span><span class="sxs-lookup"><span data-stu-id="5ee8b-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee8b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ee8b-107">DESCRIPTION</span></span>
<span data-ttu-id="5ee8b-108">Cmdleten **set-AzManagedApplicationDefinition-** hanterade program definitioner</span><span class="sxs-lookup"><span data-stu-id="5ee8b-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="5ee8b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ee8b-109">EXAMPLES</span></span>

### <span data-ttu-id="5ee8b-110">Exempel 1: definitions beskrivning för uppdatera hanterade program</span><span class="sxs-lookup"><span data-stu-id="5ee8b-110">Example 1: Update managed application definition description</span></span>
```powershell
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="5ee8b-111">Det här kommandot uppdaterar definitionen för definition av hanterade program</span><span class="sxs-lookup"><span data-stu-id="5ee8b-111">This command updates the managed application definition description</span></span>

### <span data-ttu-id="5ee8b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5ee8b-112">Example 2</span></span>

<span data-ttu-id="5ee8b-113">Definition av hanterade program uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-113">Updates managed application definition.</span></span> <span data-ttu-id="5ee8b-114">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="5ee8b-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzManagedApplicationDefinition -Id '/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef' -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip
```

## <span data-ttu-id="5ee8b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ee8b-115">PARAMETERS</span></span>

### <span data-ttu-id="5ee8b-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5ee8b-116">-ApiVersion</span></span>
<span data-ttu-id="5ee8b-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5ee8b-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="5ee8b-119">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="5ee8b-119">-Authorization</span></span>
<span data-ttu-id="5ee8b-120">Tillstånd för hanterade program definitioner.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-120">The managed application definition authorization.</span></span>
<span data-ttu-id="5ee8b-121">Semikolonavgränsade par i ett format med \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="5ee8b-121">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="5ee8b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee8b-122">-DefaultProfile</span></span>
<span data-ttu-id="5ee8b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ee8b-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5ee8b-124">-Description</span></span>
<span data-ttu-id="5ee8b-125">Definitions beskrivning för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-125">The managed application definition description.</span></span>

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

### <span data-ttu-id="5ee8b-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5ee8b-126">-DisplayName</span></span>
<span data-ttu-id="5ee8b-127">Det hanterade visnings namnet för program definitionen.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-127">The managed application definition display name.</span></span>

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

### <span data-ttu-id="5ee8b-128">-ID</span><span class="sxs-lookup"><span data-stu-id="5ee8b-128">-Id</span></span>
<span data-ttu-id="5ee8b-129">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-129">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="5ee8b-130">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee8b-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="5ee8b-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ee8b-131">-Name</span></span>
<span data-ttu-id="5ee8b-132">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="5ee8b-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="5ee8b-133">-PackageFileUri</span></span>
<span data-ttu-id="5ee8b-134">Fil-URI för det hanterade programpaketet.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="5ee8b-135">-För</span><span class="sxs-lookup"><span data-stu-id="5ee8b-135">-Pre</span></span>
<span data-ttu-id="5ee8b-136">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5ee8b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ee8b-137">-ResourceGroupName</span></span>
<span data-ttu-id="5ee8b-138">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-138">The resource group name.</span></span>

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

### <span data-ttu-id="5ee8b-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5ee8b-139">-Tag</span></span>
<span data-ttu-id="5ee8b-140">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="5ee8b-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ee8b-141">-Confirm</span></span>
<span data-ttu-id="5ee8b-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ee8b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee8b-143">-WhatIf</span></span>
<span data-ttu-id="5ee8b-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee8b-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ee8b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee8b-146">CommonParameters</span></span>
<span data-ttu-id="5ee8b-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee8b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee8b-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ee8b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee8b-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ee8b-149">INPUTS</span></span>

### <span data-ttu-id="5ee8b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5ee8b-150">System.String</span></span>

### <span data-ttu-id="5ee8b-151">System. string []</span><span class="sxs-lookup"><span data-stu-id="5ee8b-151">System.String[]</span></span>

### <span data-ttu-id="5ee8b-152">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5ee8b-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5ee8b-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ee8b-153">OUTPUTS</span></span>

### <span data-ttu-id="5ee8b-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5ee8b-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5ee8b-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ee8b-155">NOTES</span></span>

## <span data-ttu-id="5ee8b-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ee8b-156">RELATED LINKS</span></span>