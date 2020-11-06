---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4dc41f7510789664b5c453285ebea032c24f3ac7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574530"
---
# <span data-ttu-id="5ab90-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="5ab90-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="5ab90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ab90-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab90-103">Definition av hanterade program uppdateringar</span><span class="sxs-lookup"><span data-stu-id="5ab90-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ab90-104">SYNTAX</span></span>

### <span data-ttu-id="5ab90-105">Parameter uppsättning för hanterade program namn.</span><span class="sxs-lookup"><span data-stu-id="5ab90-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="5ab90-106">Vis</span><span class="sxs-lookup"><span data-stu-id="5ab90-106">(Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ab90-107">Parameter uppsättning för definition av hanterade program.</span><span class="sxs-lookup"><span data-stu-id="5ab90-107">The managed application definition Id parameter set.</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab90-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ab90-108">DESCRIPTION</span></span>
<span data-ttu-id="5ab90-109">Cmdleten **set-AzureRmManagedApplicationDefinition-** hanterade program definitioner</span><span class="sxs-lookup"><span data-stu-id="5ab90-109">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="5ab90-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ab90-110">EXAMPLES</span></span>

### <span data-ttu-id="5ab90-111">Exempel 1: definitions beskrivning för uppdatera hanterade program</span><span class="sxs-lookup"><span data-stu-id="5ab90-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="5ab90-112">Det här kommandot uppdaterar definitionen för definition av hanterade program</span><span class="sxs-lookup"><span data-stu-id="5ab90-112">This command updates the managed application definition description</span></span>

## <span data-ttu-id="5ab90-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ab90-113">PARAMETERS</span></span>

### <span data-ttu-id="5ab90-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5ab90-114">-ApiVersion</span></span>
<span data-ttu-id="5ab90-115">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5ab90-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5ab90-116">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="5ab90-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="5ab90-117">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="5ab90-117">-Authorization</span></span>
<span data-ttu-id="5ab90-118">Tillstånd för hanterade program definitioner.</span><span class="sxs-lookup"><span data-stu-id="5ab90-118">The managed application definition authorization.</span></span>
<span data-ttu-id="5ab90-119">Semikolonavgränsade par i ett format med \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="5ab90-119">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="5ab90-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab90-120">-DefaultProfile</span></span>
<span data-ttu-id="5ab90-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ab90-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab90-122">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5ab90-122">-Description</span></span>
<span data-ttu-id="5ab90-123">Definitions beskrivning för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="5ab90-123">The managed application definition description.</span></span>

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

### <span data-ttu-id="5ab90-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5ab90-124">-DisplayName</span></span>
<span data-ttu-id="5ab90-125">Det hanterade visnings namnet för program definitionen.</span><span class="sxs-lookup"><span data-stu-id="5ab90-125">The managed application definition display name.</span></span>

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

### <span data-ttu-id="5ab90-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ab90-126">-Name</span></span>
<span data-ttu-id="5ab90-127">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="5ab90-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab90-128">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="5ab90-128">-PackageFileUri</span></span>
<span data-ttu-id="5ab90-129">Fil-URI för det hanterade programpaketet.</span><span class="sxs-lookup"><span data-stu-id="5ab90-129">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="5ab90-130">-För</span><span class="sxs-lookup"><span data-stu-id="5ab90-130">-Pre</span></span>
<span data-ttu-id="5ab90-131">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5ab90-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5ab90-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab90-132">-ResourceGroupName</span></span>
<span data-ttu-id="5ab90-133">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5ab90-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab90-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5ab90-134">-Tag</span></span>
<span data-ttu-id="5ab90-135">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="5ab90-135">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="5ab90-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ab90-136">-Confirm</span></span>
<span data-ttu-id="5ab90-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ab90-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab90-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab90-138">-WhatIf</span></span>
<span data-ttu-id="5ab90-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ab90-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab90-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ab90-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab90-141">-ID</span><span class="sxs-lookup"><span data-stu-id="5ab90-141">-Id</span></span>
<span data-ttu-id="5ab90-142">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5ab90-142">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="5ab90-143">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="5ab90-143">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab90-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab90-144">CommonParameters</span></span>
<span data-ttu-id="5ab90-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab90-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab90-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab90-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab90-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ab90-147">INPUTS</span></span>

### <span data-ttu-id="5ab90-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab90-148">System.String</span></span>
<span data-ttu-id="5ab90-149">System. string [] system. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5ab90-149">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="5ab90-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ab90-150">OUTPUTS</span></span>

### <span data-ttu-id="5ab90-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5ab90-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5ab90-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ab90-152">NOTES</span></span>

## <span data-ttu-id="5ab90-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ab90-153">RELATED LINKS</span></span>

