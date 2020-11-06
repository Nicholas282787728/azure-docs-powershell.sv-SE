---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: ea36cf36b32df4c61c159e89cfdae12acdcc9509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579424"
---
# <span data-ttu-id="d016c-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d016c-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="d016c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d016c-102">SYNOPSIS</span></span>
<span data-ttu-id="d016c-103">Skapar en definition för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d016c-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d016c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d016c-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d016c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d016c-105">DESCRIPTION</span></span>
<span data-ttu-id="d016c-106">Cmdleten **New-AzureRmPolicySetDefinition** skapar en definition för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d016c-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="d016c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d016c-107">EXAMPLES</span></span>

### <span data-ttu-id="d016c-108">Exempel 1: skapa en definition för princip uppsättning med hjälp av en princip uppsättnings fil</span><span class="sxs-lookup"><span data-stu-id="d016c-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="d016c-109">Det här kommandot skapar en princip uppsättnings definition med namnet VMPolicyDefinition som innehåller de princip definitioner som anges i C:\VMPolicy.jspå.</span><span class="sxs-lookup"><span data-stu-id="d016c-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="d016c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d016c-110">PARAMETERS</span></span>

### <span data-ttu-id="d016c-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d016c-111">-ApiVersion</span></span>
<span data-ttu-id="d016c-112">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d016c-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d016c-113">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="d016c-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d016c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d016c-114">-DefaultProfile</span></span>
<span data-ttu-id="d016c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d016c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d016c-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d016c-116">-Description</span></span>
<span data-ttu-id="d016c-117">Beskrivningen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="d016c-117">The description for policy set definition.</span></span>

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

### <span data-ttu-id="d016c-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d016c-118">-DisplayName</span></span>
<span data-ttu-id="d016c-119">Visnings namnet för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="d016c-119">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="d016c-120">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d016c-120">-Metadata</span></span>
<span data-ttu-id="d016c-121">Metadata för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="d016c-121">The metadata for policy set definition.</span></span> <span data-ttu-id="d016c-122">Det kan antingen vara en sökväg till ett fil namn som innehåller metadata, eller metadata som sträng</span><span class="sxs-lookup"><span data-stu-id="d016c-122">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="d016c-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d016c-123">-Name</span></span>
<span data-ttu-id="d016c-124">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="d016c-124">The policy set definition name.</span></span>

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

### <span data-ttu-id="d016c-125">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d016c-125">-Parameter</span></span>
<span data-ttu-id="d016c-126">Parameter deklarationen för princip uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="d016c-126">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="d016c-127">Det kan antingen vara en sökväg till ett fil namn som innehåller parameter deklarationen eller parameter deklarationen som sträng.</span><span class="sxs-lookup"><span data-stu-id="d016c-127">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d016c-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d016c-128">-PolicyDefinition</span></span>
<span data-ttu-id="d016c-129">Den här definitionen av princip uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="d016c-129">The policy set definition.</span></span> <span data-ttu-id="d016c-130">Det kan antingen vara en sökväg till ett fil namn som innehåller princip definitionerna, eller så är princip uppsättnings definitionen som sträng.</span><span class="sxs-lookup"><span data-stu-id="d016c-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="d016c-131">-För</span><span class="sxs-lookup"><span data-stu-id="d016c-131">-Pre</span></span>
<span data-ttu-id="d016c-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="d016c-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d016c-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d016c-133">-Confirm</span></span>
<span data-ttu-id="d016c-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d016c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d016c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d016c-135">-WhatIf</span></span>
<span data-ttu-id="d016c-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d016c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d016c-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d016c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d016c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d016c-138">CommonParameters</span></span>
<span data-ttu-id="d016c-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d016c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d016c-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d016c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d016c-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d016c-141">INPUTS</span></span>

### <span data-ttu-id="d016c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d016c-142">System.String</span></span>

## <span data-ttu-id="d016c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d016c-143">OUTPUTS</span></span>

### <span data-ttu-id="d016c-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d016c-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d016c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d016c-145">NOTES</span></span>

## <span data-ttu-id="d016c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d016c-146">RELATED LINKS</span></span>
