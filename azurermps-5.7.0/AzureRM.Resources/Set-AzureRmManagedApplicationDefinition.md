---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 8914b6d48b14ea372f29a6b7b0f5c9a1c32a6fd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573300"
---
# <span data-ttu-id="6cc50-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="6cc50-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="6cc50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cc50-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc50-103">Definition av hanterade program uppdateringar</span><span class="sxs-lookup"><span data-stu-id="6cc50-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cc50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cc50-104">SYNTAX</span></span>

### <span data-ttu-id="6cc50-105">SetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="6cc50-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cc50-106">SetById</span><span class="sxs-lookup"><span data-stu-id="6cc50-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc50-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cc50-107">DESCRIPTION</span></span>
<span data-ttu-id="6cc50-108">Cmdleten **set-AzureRmManagedApplicationDefinition-** hanterade program definitioner</span><span class="sxs-lookup"><span data-stu-id="6cc50-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="6cc50-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cc50-109">EXAMPLES</span></span>

### <span data-ttu-id="6cc50-110">Exempel 1: definitions beskrivning för uppdatera hanterade program</span><span class="sxs-lookup"><span data-stu-id="6cc50-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="6cc50-111">Det här kommandot uppdaterar definitionen för definition av hanterade program</span><span class="sxs-lookup"><span data-stu-id="6cc50-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="6cc50-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cc50-112">PARAMETERS</span></span>

### <span data-ttu-id="6cc50-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6cc50-113">-ApiVersion</span></span>
<span data-ttu-id="6cc50-114">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6cc50-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6cc50-115">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="6cc50-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-116">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="6cc50-116">-Authorization</span></span>
<span data-ttu-id="6cc50-117">Tillstånd för hanterade program definitioner.</span><span class="sxs-lookup"><span data-stu-id="6cc50-117">The managed application definition authorization.</span></span>
<span data-ttu-id="6cc50-118">Semikolonavgränsade par i ett format med \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="6cc50-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc50-119">-DefaultProfile</span></span>
<span data-ttu-id="6cc50-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc50-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6cc50-121">-Description</span></span>
<span data-ttu-id="6cc50-122">Definitions beskrivning för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="6cc50-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6cc50-123">-DisplayName</span></span>
<span data-ttu-id="6cc50-124">Det hanterade visnings namnet för program definitionen.</span><span class="sxs-lookup"><span data-stu-id="6cc50-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-125">-ID</span><span class="sxs-lookup"><span data-stu-id="6cc50-125">-Id</span></span>
<span data-ttu-id="6cc50-126">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6cc50-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="6cc50-127">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc50-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="6cc50-128">-Name</span></span>
<span data-ttu-id="6cc50-129">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="6cc50-129">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="6cc50-130">-PackageFileUri</span></span>
<span data-ttu-id="6cc50-131">Fil-URI för det hanterade programpaketet.</span><span class="sxs-lookup"><span data-stu-id="6cc50-131">The managed application definition package file uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-132">-För</span><span class="sxs-lookup"><span data-stu-id="6cc50-132">-Pre</span></span>
<span data-ttu-id="6cc50-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6cc50-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc50-134">-ResourceGroupName</span></span>
<span data-ttu-id="6cc50-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6cc50-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6cc50-136">-Tag</span></span>
<span data-ttu-id="6cc50-137">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="6cc50-137">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6cc50-138">-Confirm</span></span>
<span data-ttu-id="6cc50-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6cc50-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc50-140">-WhatIf</span></span>
<span data-ttu-id="6cc50-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6cc50-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cc50-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6cc50-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc50-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc50-143">CommonParameters</span></span>
<span data-ttu-id="6cc50-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc50-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc50-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc50-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc50-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cc50-146">INPUTS</span></span>

### <span data-ttu-id="6cc50-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6cc50-147">System.String</span></span>
<span data-ttu-id="6cc50-148">System. string [] system. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6cc50-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="6cc50-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cc50-149">OUTPUTS</span></span>

### <span data-ttu-id="6cc50-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6cc50-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6cc50-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cc50-151">NOTES</span></span>

## <span data-ttu-id="6cc50-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cc50-152">RELATED LINKS</span></span>
