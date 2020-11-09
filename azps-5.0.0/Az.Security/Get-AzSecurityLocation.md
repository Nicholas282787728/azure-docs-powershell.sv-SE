---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324264"
---
# <span data-ttu-id="9aa13-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="9aa13-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="9aa13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9aa13-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa13-103">Hämtar den plats där Azure Security Center automatiskt sparar data för det specifika abonnemanget</span><span class="sxs-lookup"><span data-stu-id="9aa13-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="9aa13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9aa13-104">SYNTAX</span></span>

### <span data-ttu-id="9aa13-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="9aa13-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aa13-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="9aa13-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aa13-107">ID</span><span class="sxs-lookup"><span data-stu-id="9aa13-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9aa13-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9aa13-108">DESCRIPTION</span></span>
<span data-ttu-id="9aa13-109">Azure Security Center bestämmer automatiskt var de ska sparas.</span><span class="sxs-lookup"><span data-stu-id="9aa13-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="9aa13-110">Använd denna cmdlet för att identifiera platsen.</span><span class="sxs-lookup"><span data-stu-id="9aa13-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="9aa13-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9aa13-111">EXAMPLES</span></span>

### <span data-ttu-id="9aa13-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9aa13-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="9aa13-113">Hämtar den plats där de beräknade säkerhets uppgifterna sparas i Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="9aa13-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="9aa13-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9aa13-114">PARAMETERS</span></span>

### <span data-ttu-id="9aa13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa13-115">-DefaultProfile</span></span>
<span data-ttu-id="9aa13-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9aa13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aa13-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="9aa13-117">-Name</span></span>
<span data-ttu-id="9aa13-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="9aa13-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa13-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9aa13-119">-ResourceId</span></span>
<span data-ttu-id="9aa13-120">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9aa13-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa13-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa13-121">CommonParameters</span></span>
<span data-ttu-id="9aa13-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aa13-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa13-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9aa13-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa13-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9aa13-124">INPUTS</span></span>

### <span data-ttu-id="9aa13-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9aa13-125">System.String</span></span>

## <span data-ttu-id="9aa13-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9aa13-126">OUTPUTS</span></span>

### <span data-ttu-id="9aa13-127">Microsoft. Azure. commands. Security. Models. locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="9aa13-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="9aa13-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9aa13-128">NOTES</span></span>

## <span data-ttu-id="9aa13-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9aa13-129">RELATED LINKS</span></span>
