---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: 3d6a5488e7e101c904e90d056c8b2ffc03e786fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923786"
---
# <span data-ttu-id="f917f-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="f917f-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="f917f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f917f-102">SYNOPSIS</span></span>
<span data-ttu-id="f917f-103">Definition av hanterade program uppdateringar</span><span class="sxs-lookup"><span data-stu-id="f917f-103">Updates managed application definition</span></span>

## <span data-ttu-id="f917f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f917f-104">SYNTAX</span></span>

### <span data-ttu-id="f917f-105">SetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="f917f-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f917f-106">SetById</span><span class="sxs-lookup"><span data-stu-id="f917f-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f917f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f917f-107">DESCRIPTION</span></span>
<span data-ttu-id="f917f-108">Cmdleten **set-AzManagedApplicationDefinition-** hanterade program definitioner</span><span class="sxs-lookup"><span data-stu-id="f917f-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="f917f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f917f-109">EXAMPLES</span></span>

### <span data-ttu-id="f917f-110">Exempel 1: definitions beskrivning för uppdatera hanterade program</span><span class="sxs-lookup"><span data-stu-id="f917f-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="f917f-111">Det här kommandot uppdaterar definitionen för definition av hanterade program</span><span class="sxs-lookup"><span data-stu-id="f917f-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="f917f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f917f-112">PARAMETERS</span></span>

### <span data-ttu-id="f917f-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f917f-113">-ApiVersion</span></span>
<span data-ttu-id="f917f-114">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f917f-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f917f-115">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="f917f-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f917f-116">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="f917f-116">-Authorization</span></span>
<span data-ttu-id="f917f-117">Tillstånd för hanterade program definitioner.</span><span class="sxs-lookup"><span data-stu-id="f917f-117">The managed application definition authorization.</span></span>
<span data-ttu-id="f917f-118">Semikolonavgränsade par i ett format med \< principalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="f917f-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="f917f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f917f-119">-DefaultProfile</span></span>
<span data-ttu-id="f917f-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f917f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f917f-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f917f-121">-Description</span></span>
<span data-ttu-id="f917f-122">Definitions beskrivning för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="f917f-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="f917f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f917f-123">-DisplayName</span></span>
<span data-ttu-id="f917f-124">Det hanterade visnings namnet för program definitionen.</span><span class="sxs-lookup"><span data-stu-id="f917f-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="f917f-125">-ID</span><span class="sxs-lookup"><span data-stu-id="f917f-125">-Id</span></span>
<span data-ttu-id="f917f-126">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f917f-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="f917f-127">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f917f-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="f917f-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="f917f-128">-Name</span></span>
<span data-ttu-id="f917f-129">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="f917f-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="f917f-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="f917f-130">-PackageFileUri</span></span>
<span data-ttu-id="f917f-131">Fil-URI för det hanterade programpaketet.</span><span class="sxs-lookup"><span data-stu-id="f917f-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="f917f-132">-För</span><span class="sxs-lookup"><span data-stu-id="f917f-132">-Pre</span></span>
<span data-ttu-id="f917f-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f917f-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f917f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f917f-134">-ResourceGroupName</span></span>
<span data-ttu-id="f917f-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f917f-135">The resource group name.</span></span>

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

### <span data-ttu-id="f917f-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f917f-136">-Tag</span></span>
<span data-ttu-id="f917f-137">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="f917f-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f917f-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f917f-138">-Confirm</span></span>
<span data-ttu-id="f917f-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f917f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f917f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f917f-140">-WhatIf</span></span>
<span data-ttu-id="f917f-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f917f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f917f-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f917f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f917f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f917f-143">CommonParameters</span></span>
<span data-ttu-id="f917f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f917f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f917f-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f917f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f917f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f917f-146">INPUTS</span></span>

### <span data-ttu-id="f917f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f917f-147">System.String</span></span>

### <span data-ttu-id="f917f-148">System. string []</span><span class="sxs-lookup"><span data-stu-id="f917f-148">System.String[]</span></span>

### <span data-ttu-id="f917f-149">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f917f-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f917f-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f917f-150">OUTPUTS</span></span>

### <span data-ttu-id="f917f-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f917f-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f917f-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f917f-152">NOTES</span></span>

## <span data-ttu-id="f917f-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f917f-153">RELATED LINKS</span></span>
