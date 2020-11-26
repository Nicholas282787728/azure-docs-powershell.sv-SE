---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261708"
---
# <span data-ttu-id="2a725-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2a725-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="2a725-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a725-102">SYNOPSIS</span></span>
<span data-ttu-id="2a725-103">Skapa ny rekommendations konfiguration för IoT-säkerhetslösning</span><span class="sxs-lookup"><span data-stu-id="2a725-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="2a725-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a725-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a725-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a725-105">DESCRIPTION</span></span>
<span data-ttu-id="2a725-106">AzIotSecuritySolutionRecommendationConfigurationObject skapar ett nytt rekommendations konfigurations objekt för IoT-säkerhetslösning.</span><span class="sxs-lookup"><span data-stu-id="2a725-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="2a725-107">På så sätt konfigureras statusen för en rekommendation, oavsett om den är aktive rad eller inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="2a725-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="2a725-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a725-108">EXAMPLES</span></span>

### <span data-ttu-id="2a725-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a725-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="2a725-110">Skapa en ny rekommendations konfiguration för rekommendations typ "IoT_ACRAuthentication" med status inställd på Disable</span><span class="sxs-lookup"><span data-stu-id="2a725-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="2a725-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a725-111">PARAMETERS</span></span>

### <span data-ttu-id="2a725-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a725-112">-DefaultProfile</span></span>
<span data-ttu-id="2a725-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a725-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a725-114">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="2a725-114">-Enabled</span></span>
<span data-ttu-id="2a725-115">Status.</span><span class="sxs-lookup"><span data-stu-id="2a725-115">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a725-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="2a725-116">-RecommendationType</span></span>
<span data-ttu-id="2a725-117">Typ av rekommendation.</span><span class="sxs-lookup"><span data-stu-id="2a725-117">Recommendation type.</span></span>

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

### <span data-ttu-id="2a725-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a725-118">CommonParameters</span></span>
<span data-ttu-id="2a725-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a725-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a725-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a725-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a725-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a725-121">INPUTS</span></span>

### <span data-ttu-id="2a725-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="2a725-122">None</span></span>

## <span data-ttu-id="2a725-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a725-123">OUTPUTS</span></span>

### <span data-ttu-id="2a725-124">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a725-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="2a725-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a725-125">NOTES</span></span>

## <span data-ttu-id="2a725-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a725-126">RELATED LINKS</span></span>