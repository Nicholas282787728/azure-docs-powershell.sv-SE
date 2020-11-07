---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575863"
---
# <span data-ttu-id="f5497-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5497-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="f5497-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5497-102">SYNOPSIS</span></span>
<span data-ttu-id="f5497-103">Söker efter resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="f5497-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5497-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5497-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5497-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5497-105">DESCRIPTION</span></span>
<span data-ttu-id="f5497-106">Cmdleten **find-AzureRmResourceGroup** söker efter resurs grupper med de angivna parametrarna.</span><span class="sxs-lookup"><span data-stu-id="f5497-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="f5497-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5497-107">EXAMPLES</span></span>

### <span data-ttu-id="f5497-108">Exempel 1: Sök efter alla resurs grupper</span><span class="sxs-lookup"><span data-stu-id="f5497-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="f5497-109">Det här kommandot hittar alla resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="f5497-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="f5497-110">Exempel 2: Sök efter resurs grupper efter taggnamn</span><span class="sxs-lookup"><span data-stu-id="f5497-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="f5497-111">Det här kommandot hittar alla resurs grupper som har en tagg som heter testtag.</span><span class="sxs-lookup"><span data-stu-id="f5497-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="f5497-112">Exempel 3: Sök efter resurs grupper efter taggnamn och värde</span><span class="sxs-lookup"><span data-stu-id="f5497-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="f5497-113">Det här kommandot hittar alla resurs grupper som har en tagg med namnet testtag och värdet testval.</span><span class="sxs-lookup"><span data-stu-id="f5497-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="f5497-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5497-114">PARAMETERS</span></span>

### <span data-ttu-id="f5497-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f5497-115">-ApiVersion</span></span>
<span data-ttu-id="f5497-116">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f5497-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="f5497-117">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="f5497-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f5497-118">-För</span><span class="sxs-lookup"><span data-stu-id="f5497-118">-Pre</span></span>
<span data-ttu-id="f5497-119">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f5497-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f5497-120">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f5497-120">-Tag</span></span>
<span data-ttu-id="f5497-121">Anger taggnings information som en hash-tabell för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="f5497-121">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="f5497-122">Använd följande format:</span><span class="sxs-lookup"><span data-stu-id="f5497-122">Use the following formats:</span></span>

<span data-ttu-id="f5497-123">@ {tagName = $null} eller @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="f5497-123">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5497-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5497-124">-DefaultProfile</span></span>
<span data-ttu-id="f5497-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5497-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5497-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5497-126">CommonParameters</span></span>
<span data-ttu-id="f5497-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5497-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5497-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5497-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5497-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5497-129">INPUTS</span></span>

## <span data-ttu-id="f5497-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5497-130">OUTPUTS</span></span>

### <span data-ttu-id="f5497-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f5497-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f5497-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5497-132">NOTES</span></span>

## <span data-ttu-id="f5497-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5497-133">RELATED LINKS</span></span>
