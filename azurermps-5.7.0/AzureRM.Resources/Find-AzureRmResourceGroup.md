---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 42e268a36cf6ea45d4a36ef1a7c3edd825c6e8ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579448"
---
# <span data-ttu-id="cdc78-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cdc78-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="cdc78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdc78-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc78-103">Söker efter resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="cdc78-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdc78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdc78-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdc78-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc78-106">Cmdleten **find-AzureRmResourceGroup** söker efter resurs grupper med de angivna parametrarna.</span><span class="sxs-lookup"><span data-stu-id="cdc78-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="cdc78-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdc78-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc78-108">Exempel 1: Sök efter alla resurs grupper</span><span class="sxs-lookup"><span data-stu-id="cdc78-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="cdc78-109">Det här kommandot hittar alla resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="cdc78-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="cdc78-110">Exempel 2: Sök efter resurs grupper efter taggnamn</span><span class="sxs-lookup"><span data-stu-id="cdc78-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="cdc78-111">Det här kommandot hittar alla resurs grupper som har en tagg som heter testtag.</span><span class="sxs-lookup"><span data-stu-id="cdc78-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="cdc78-112">Exempel 3: Sök efter resurs grupper efter taggnamn och värde</span><span class="sxs-lookup"><span data-stu-id="cdc78-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="cdc78-113">Det här kommandot hittar alla resurs grupper som har en tagg med namnet testtag och värdet testval.</span><span class="sxs-lookup"><span data-stu-id="cdc78-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="cdc78-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdc78-114">PARAMETERS</span></span>

### <span data-ttu-id="cdc78-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cdc78-115">-ApiVersion</span></span>
<span data-ttu-id="cdc78-116">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="cdc78-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="cdc78-117">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="cdc78-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cdc78-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc78-118">-DefaultProfile</span></span>
<span data-ttu-id="cdc78-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cdc78-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdc78-120">-För</span><span class="sxs-lookup"><span data-stu-id="cdc78-120">-Pre</span></span>
<span data-ttu-id="cdc78-121">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="cdc78-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cdc78-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cdc78-122">-Tag</span></span>
<span data-ttu-id="cdc78-123">Anger taggnings information som en hash-tabell för att filtrera resultaten.</span><span class="sxs-lookup"><span data-stu-id="cdc78-123">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="cdc78-124">Använd följande format:</span><span class="sxs-lookup"><span data-stu-id="cdc78-124">Use the following formats:</span></span>

<span data-ttu-id="cdc78-125">@ {tagName = $null} eller @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="cdc78-125">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc78-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc78-126">CommonParameters</span></span>
<span data-ttu-id="cdc78-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc78-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc78-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdc78-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc78-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdc78-129">INPUTS</span></span>

### <span data-ttu-id="cdc78-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="cdc78-130">None</span></span>
<span data-ttu-id="cdc78-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cdc78-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cdc78-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdc78-132">OUTPUTS</span></span>

### <span data-ttu-id="cdc78-133">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="cdc78-133">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cdc78-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdc78-134">NOTES</span></span>

## <span data-ttu-id="cdc78-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdc78-135">RELATED LINKS</span></span>
