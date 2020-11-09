---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322148"
---
# <span data-ttu-id="19c2d-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="19c2d-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="19c2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="19c2d-103">Skapar en definition för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="19c2d-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="19c2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19c2d-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19c2d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="19c2d-106">Cmdleten **New-AzManagedApplicationDefinition** skapar en definition av hanterad program.</span><span class="sxs-lookup"><span data-stu-id="19c2d-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="19c2d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19c2d-107">EXAMPLES</span></span>

### <span data-ttu-id="19c2d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="19c2d-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="19c2d-109">Det här kommandot skapar en definition för hanterade program</span><span class="sxs-lookup"><span data-stu-id="19c2d-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="19c2d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19c2d-110">PARAMETERS</span></span>

### <span data-ttu-id="19c2d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="19c2d-111">-ApiVersion</span></span>
<span data-ttu-id="19c2d-112">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="19c2d-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="19c2d-113">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="19c2d-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="19c2d-114">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="19c2d-114">-Authorization</span></span>
<span data-ttu-id="19c2d-115">Tillstånd för hanterade program definitioner.</span><span class="sxs-lookup"><span data-stu-id="19c2d-115">The managed application definition authorization.</span></span>
<span data-ttu-id="19c2d-116">Semikolonavgränsade par i ett format med \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="19c2d-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c2d-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="19c2d-117">-CreateUiDefinition</span></span>
<span data-ttu-id="19c2d-118">Definitionen av skapa användar gränssnitt i definitionen av hanterade program</span><span class="sxs-lookup"><span data-stu-id="19c2d-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="19c2d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c2d-119">-DefaultProfile</span></span>
<span data-ttu-id="19c2d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19c2d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19c2d-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="19c2d-121">-Description</span></span>
<span data-ttu-id="19c2d-122">Definitions beskrivning för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="19c2d-122">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c2d-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="19c2d-123">-DisplayName</span></span>
<span data-ttu-id="19c2d-124">Det hanterade visnings namnet för program definitionen.</span><span class="sxs-lookup"><span data-stu-id="19c2d-124">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c2d-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="19c2d-125">-Location</span></span>
<span data-ttu-id="19c2d-126">Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="19c2d-126">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c2d-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="19c2d-127">-LockLevel</span></span>
<span data-ttu-id="19c2d-128">Nivån på definitionen för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="19c2d-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c2d-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="19c2d-129">-MainTemplate</span></span>
<span data-ttu-id="19c2d-130">Huvud mal len för hanterade program definitioner</span><span class="sxs-lookup"><span data-stu-id="19c2d-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="19c2d-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="19c2d-131">-Name</span></span>
<span data-ttu-id="19c2d-132">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="19c2d-132">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c2d-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="19c2d-133">-PackageFileUri</span></span>
<span data-ttu-id="19c2d-134">Fil-URI för det hanterade programpaketet.</span><span class="sxs-lookup"><span data-stu-id="19c2d-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="19c2d-135">-För</span><span class="sxs-lookup"><span data-stu-id="19c2d-135">-Pre</span></span>
<span data-ttu-id="19c2d-136">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="19c2d-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="19c2d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c2d-137">-ResourceGroupName</span></span>
<span data-ttu-id="19c2d-138">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="19c2d-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c2d-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="19c2d-139">-Tag</span></span>
<span data-ttu-id="19c2d-140">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="19c2d-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="19c2d-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="19c2d-141">-Confirm</span></span>
<span data-ttu-id="19c2d-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19c2d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c2d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c2d-143">-WhatIf</span></span>
<span data-ttu-id="19c2d-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="19c2d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c2d-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="19c2d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c2d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c2d-146">CommonParameters</span></span>
<span data-ttu-id="19c2d-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c2d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c2d-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19c2d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c2d-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19c2d-149">INPUTS</span></span>

### <span data-ttu-id="19c2d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="19c2d-150">System.String</span></span>

### <span data-ttu-id="19c2d-151">Microsoft. Azure. kommandon. ResourceManager. cmdlets. entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="19c2d-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="19c2d-152">System. string []</span><span class="sxs-lookup"><span data-stu-id="19c2d-152">System.String[]</span></span>

### <span data-ttu-id="19c2d-153">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="19c2d-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="19c2d-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19c2d-154">OUTPUTS</span></span>

### <span data-ttu-id="19c2d-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="19c2d-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="19c2d-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19c2d-156">NOTES</span></span>

## <span data-ttu-id="19c2d-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19c2d-157">RELATED LINKS</span></span>
