---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 5574966734c3b35bd5b104addf1872a85eb9660b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576421"
---
# <span data-ttu-id="fe1f9-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="fe1f9-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="fe1f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1f9-103">Skapar en definition för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe1f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe1f9-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe1f9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe1f9-105">DESCRIPTION</span></span>
<span data-ttu-id="fe1f9-106">Cmdleten **New-AzureRmManagedApplicationDefinition** skapar en definition av hanterad program.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="fe1f9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe1f9-107">EXAMPLES</span></span>

### <span data-ttu-id="fe1f9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe1f9-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="fe1f9-109">Det här kommandot skapar en definition för hanterade program</span><span class="sxs-lookup"><span data-stu-id="fe1f9-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="fe1f9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe1f9-110">PARAMETERS</span></span>

### <span data-ttu-id="fe1f9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe1f9-111">-ApiVersion</span></span>
<span data-ttu-id="fe1f9-112">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fe1f9-113">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fe1f9-114">-Auktorisering</span><span class="sxs-lookup"><span data-stu-id="fe1f9-114">-Authorization</span></span>
<span data-ttu-id="fe1f9-115">Tillstånd för hanterade program definitioner.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-115">The managed application definition authorization.</span></span>
<span data-ttu-id="fe1f9-116">Semikolonavgränsade par i ett format med \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="fe1f9-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f9-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="fe1f9-117">-CreateUiDefinition</span></span>
<span data-ttu-id="fe1f9-118">Definitionen av skapa användar gränssnitt i definitionen av hanterade program</span><span class="sxs-lookup"><span data-stu-id="fe1f9-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="fe1f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1f9-119">-DefaultProfile</span></span>
<span data-ttu-id="fe1f9-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe1f9-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="fe1f9-121">-Description</span></span>
<span data-ttu-id="fe1f9-122">Definitions beskrivning för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f9-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe1f9-123">-DisplayName</span></span>
<span data-ttu-id="fe1f9-124">Det hanterade visnings namnet för program definitionen.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f9-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="fe1f9-125">-Location</span></span>
<span data-ttu-id="fe1f9-126">Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-126">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f9-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="fe1f9-127">-LockLevel</span></span>
<span data-ttu-id="fe1f9-128">Nivån på definitionen för hanterade program.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f9-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="fe1f9-129">-MainTemplate</span></span>
<span data-ttu-id="fe1f9-130">Huvud mal len för hanterade program definitioner</span><span class="sxs-lookup"><span data-stu-id="fe1f9-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="fe1f9-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe1f9-131">-Name</span></span>
<span data-ttu-id="fe1f9-132">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-132">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f9-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="fe1f9-133">-PackageFileUri</span></span>
<span data-ttu-id="fe1f9-134">Fil-URI för det hanterade programpaketet.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="fe1f9-135">-För</span><span class="sxs-lookup"><span data-stu-id="fe1f9-135">-Pre</span></span>
<span data-ttu-id="fe1f9-136">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fe1f9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe1f9-137">-ResourceGroupName</span></span>
<span data-ttu-id="fe1f9-138">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f9-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fe1f9-139">-Tag</span></span>
<span data-ttu-id="fe1f9-140">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fe1f9-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fe1f9-141">-Confirm</span></span>
<span data-ttu-id="fe1f9-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe1f9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe1f9-143">-WhatIf</span></span>
<span data-ttu-id="fe1f9-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe1f9-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe1f9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1f9-146">CommonParameters</span></span>
<span data-ttu-id="fe1f9-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe1f9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1f9-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1f9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1f9-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe1f9-149">INPUTS</span></span>

### <span data-ttu-id="fe1f9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="fe1f9-150">System.String</span></span>
<span data-ttu-id="fe1f9-151">Microsoft. Azure. kommandon. ResourceManager. cmdlets. deentities. Application. ApplicationLockLevel system. string [] system. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="fe1f9-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="fe1f9-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe1f9-152">OUTPUTS</span></span>

### <span data-ttu-id="fe1f9-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fe1f9-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fe1f9-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe1f9-154">NOTES</span></span>

## <span data-ttu-id="fe1f9-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe1f9-155">RELATED LINKS</span></span>