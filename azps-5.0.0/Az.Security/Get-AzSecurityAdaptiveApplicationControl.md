---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324270"
---
# <span data-ttu-id="39dc9-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="39dc9-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="39dc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="39dc9-103">Hämtar en lista med program kontroll för den virtuella dator/server gruppen för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="39dc9-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="39dc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39dc9-104">SYNTAX</span></span>

### <span data-ttu-id="39dc9-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="39dc9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39dc9-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39dc9-106">DESCRIPTION</span></span>
<span data-ttu-id="39dc9-107">Anpassade program kontroller beräknas automatiskt i Azure Security Center, Använd denna cmdlet för att få en lista över anpassade program styr resurser i ett abonnemangs omfång.</span><span class="sxs-lookup"><span data-stu-id="39dc9-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="39dc9-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39dc9-108">EXAMPLES</span></span>

### <span data-ttu-id="39dc9-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="39dc9-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="39dc9-110">Hämtar en lista med program kontroll för den virtuella dator/server gruppen för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="39dc9-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="39dc9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39dc9-111">PARAMETERS</span></span>

### <span data-ttu-id="39dc9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39dc9-112">-DefaultProfile</span></span>
<span data-ttu-id="39dc9-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39dc9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39dc9-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39dc9-114">-SubscriptionId</span></span>
<span data-ttu-id="39dc9-115">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="39dc9-115">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39dc9-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="39dc9-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="39dc9-117">Inkludera policy reglerna.</span><span class="sxs-lookup"><span data-stu-id="39dc9-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39dc9-118">-Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39dc9-118">-Summary</span></span>
<span data-ttu-id="39dc9-119">Returnera utdata i ett summeradt formulär.</span><span class="sxs-lookup"><span data-stu-id="39dc9-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39dc9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39dc9-120">CommonParameters</span></span>
<span data-ttu-id="39dc9-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39dc9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39dc9-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39dc9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39dc9-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39dc9-123">INPUTS</span></span>

### <span data-ttu-id="39dc9-124">System. String</span><span class="sxs-lookup"><span data-stu-id="39dc9-124">System.String</span></span>

### <span data-ttu-id="39dc9-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39dc9-125">System.Boolean</span></span>

## <span data-ttu-id="39dc9-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39dc9-126">OUTPUTS</span></span>

### <span data-ttu-id="39dc9-127">Microsoft. Azure. commands. Security. Models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="39dc9-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="39dc9-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39dc9-128">NOTES</span></span>

## <span data-ttu-id="39dc9-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39dc9-129">RELATED LINKS</span></span>
