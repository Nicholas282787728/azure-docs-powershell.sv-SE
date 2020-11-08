---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092198"
---
# <span data-ttu-id="e58b4-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="e58b4-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="e58b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e58b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e58b4-103">Hämtar principer för princip ETA data</span><span class="sxs-lookup"><span data-stu-id="e58b4-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="e58b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e58b4-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e58b4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e58b4-105">DESCRIPTION</span></span>
<span data-ttu-id="e58b4-106">Cmdleten **Get-AzPolicyRemediation** hämtar alla principer för princip ETA data eller en viss metadatatjänst för principer.</span><span class="sxs-lookup"><span data-stu-id="e58b4-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="e58b4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e58b4-107">EXAMPLES</span></span>

### <span data-ttu-id="e58b4-108">Exempel 1: Hämta alla principer för metadatamallar</span><span class="sxs-lookup"><span data-stu-id="e58b4-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="e58b4-109">Det här kommandot får alla principer för metadatapaket</span><span class="sxs-lookup"><span data-stu-id="e58b4-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="e58b4-110">Exempel 2: Hämta en samling med tio principer för metadatapaket</span><span class="sxs-lookup"><span data-stu-id="e58b4-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="e58b4-111">Det här kommandot får en samling med tio principer för metadatapaket</span><span class="sxs-lookup"><span data-stu-id="e58b4-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="e58b4-112">Exempel 3: Hämta en enskild princip för en metadatamall med namnet ' ACF1348 '</span><span class="sxs-lookup"><span data-stu-id="e58b4-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="e58b4-113">Det här kommandot får en enskild metadatatjänst med namnet ' ACF1348 '</span><span class="sxs-lookup"><span data-stu-id="e58b4-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="e58b4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e58b4-114">PARAMETERS</span></span>

### <span data-ttu-id="e58b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e58b4-115">-DefaultProfile</span></span>
<span data-ttu-id="e58b4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e58b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e58b4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e58b4-117">-Name</span></span>
<span data-ttu-id="e58b4-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="e58b4-118">Resource name.</span></span>

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

### <span data-ttu-id="e58b4-119">-Överst</span><span class="sxs-lookup"><span data-stu-id="e58b4-119">-Top</span></span>
<span data-ttu-id="e58b4-120">Maximalt antal principer för princip som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="e58b4-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e58b4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e58b4-121">CommonParameters</span></span>
<span data-ttu-id="e58b4-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e58b4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e58b4-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e58b4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e58b4-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e58b4-124">INPUTS</span></span>

### <span data-ttu-id="e58b4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e58b4-125">System.String</span></span>

## <span data-ttu-id="e58b4-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e58b4-126">OUTPUTS</span></span>

### <span data-ttu-id="e58b4-127">Microsoft. Azure. commands. PolicyInsights. Models. PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="e58b4-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="e58b4-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e58b4-128">NOTES</span></span>

## <span data-ttu-id="e58b4-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e58b4-129">RELATED LINKS</span></span>
