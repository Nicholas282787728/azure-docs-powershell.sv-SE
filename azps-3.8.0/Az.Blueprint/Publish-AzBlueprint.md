---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: e61beaa43f881aa148401ef91cd4cb37c1f18d88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088717"
---
# <span data-ttu-id="d83fd-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="d83fd-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="d83fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d83fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d83fd-103">Publicera en ny version av en skiss.</span><span class="sxs-lookup"><span data-stu-id="d83fd-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="d83fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d83fd-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d83fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d83fd-105">DESCRIPTION</span></span>
<span data-ttu-id="d83fd-106">Publicera en ny version av en skiss definition.</span><span class="sxs-lookup"><span data-stu-id="d83fd-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="d83fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d83fd-107">EXAMPLES</span></span>

### <span data-ttu-id="d83fd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d83fd-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```
<span data-ttu-id="d83fd-109">Publicera en ny version av en skiss definition.</span><span class="sxs-lookup"><span data-stu-id="d83fd-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="d83fd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d83fd-110">PARAMETERS</span></span>

### <span data-ttu-id="d83fd-111">-Skiss</span><span class="sxs-lookup"><span data-stu-id="d83fd-111">-Blueprint</span></span>
<span data-ttu-id="d83fd-112">Skiss objekt.</span><span class="sxs-lookup"><span data-stu-id="d83fd-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d83fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83fd-113">-DefaultProfile</span></span>
<span data-ttu-id="d83fd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d83fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83fd-115">-Version</span><span class="sxs-lookup"><span data-stu-id="d83fd-115">-Version</span></span>
<span data-ttu-id="d83fd-116">Version för ritnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="d83fd-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="d83fd-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="d83fd-117">-ChangeNote</span></span>
<span data-ttu-id="d83fd-118">Anteckningar som beskriver innehållet i den här skiss versionen.</span><span class="sxs-lookup"><span data-stu-id="d83fd-118">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="d83fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83fd-119">CommonParameters</span></span>
<span data-ttu-id="d83fd-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d83fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d83fd-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83fd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83fd-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d83fd-122">INPUTS</span></span>

### <span data-ttu-id="d83fd-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d83fd-123">System.String</span></span>

### <span data-ttu-id="d83fd-124">Microsoft. Azure. commands. skissa. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="d83fd-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="d83fd-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d83fd-125">OUTPUTS</span></span>

### <span data-ttu-id="d83fd-126">Microsoft. Azure. commands. skissa. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="d83fd-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="d83fd-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d83fd-127">NOTES</span></span>

## <span data-ttu-id="d83fd-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d83fd-128">RELATED LINKS</span></span>
