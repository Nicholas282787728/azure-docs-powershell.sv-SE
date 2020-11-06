---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573899"
---
# <span data-ttu-id="3f481-101">Get-AzureRmSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="3f481-101">Get-AzureRmSecurityLocation</span></span>

## <span data-ttu-id="3f481-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f481-102">SYNOPSIS</span></span>
<span data-ttu-id="3f481-103">Hämtar den plats där Azure Security Center automatiskt sparar data för det specifika abonnemanget</span><span class="sxs-lookup"><span data-stu-id="3f481-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f481-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f481-104">SYNTAX</span></span>

### <span data-ttu-id="3f481-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="3f481-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f481-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3f481-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f481-107">ID</span><span class="sxs-lookup"><span data-stu-id="3f481-107">ResourceId</span></span>
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f481-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f481-108">DESCRIPTION</span></span>
<span data-ttu-id="3f481-109">Azure Security Center bestämmer automatiskt var de ska sparas.</span><span class="sxs-lookup"><span data-stu-id="3f481-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="3f481-110">Använd denna cmdlet för att identifiera platsen.</span><span class="sxs-lookup"><span data-stu-id="3f481-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="3f481-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f481-111">EXAMPLES</span></span>

### <span data-ttu-id="3f481-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f481-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="3f481-113">Hämtar den plats där de beräknade säkerhets uppgifterna sparas i Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="3f481-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="3f481-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f481-114">PARAMETERS</span></span>

### <span data-ttu-id="3f481-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f481-115">-DefaultProfile</span></span>
<span data-ttu-id="3f481-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f481-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f481-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f481-117">-Name</span></span>
<span data-ttu-id="3f481-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="3f481-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f481-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f481-119">-ResourceId</span></span>
<span data-ttu-id="3f481-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3f481-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f481-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f481-121">CommonParameters</span></span>
<span data-ttu-id="3f481-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f481-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f481-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f481-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f481-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f481-124">INPUTS</span></span>

### <span data-ttu-id="3f481-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3f481-125">System.String</span></span>

## <span data-ttu-id="3f481-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f481-126">OUTPUTS</span></span>

### <span data-ttu-id="3f481-127">Microsoft. Azure. commands. Security. Models. locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="3f481-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="3f481-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f481-128">NOTES</span></span>

## <span data-ttu-id="3f481-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f481-129">RELATED LINKS</span></span>
