---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityCompliance.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityCompliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityCompliance.md
ms.openlocfilehash: 1a1aa0675637bd5bbe8a8b0d4007ab426aba6592
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755680"
---
# <span data-ttu-id="d3293-101">Get-AzureRmSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="d3293-101">Get-AzureRmSecurityCompliance</span></span>

## <span data-ttu-id="d3293-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3293-102">SYNOPSIS</span></span>
<span data-ttu-id="d3293-103">Få en prenumerations säkerhet över tid</span><span class="sxs-lookup"><span data-stu-id="d3293-103">Get the security compliance of a subscription over time</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3293-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3293-104">SYNTAX</span></span>

### <span data-ttu-id="d3293-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="d3293-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityCompliance [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3293-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d3293-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityCompliance -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3293-107">ID</span><span class="sxs-lookup"><span data-stu-id="d3293-107">ResourceId</span></span>
```
Get-AzureRmSecurityCompliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3293-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3293-108">DESCRIPTION</span></span>
<span data-ttu-id="d3293-109">Hämtar säkerhetsfunktioner för ett abonnemang baserat på det aktuella alternativet för felfri och ej säkra resurser för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="d3293-109">Gets the security compliance of a subscription based on the current healthy and non secured resources ratio on this subscription.</span></span>
<span data-ttu-id="d3293-110">Säkerhetskompatibiliteten beräknas varje dag och historiken sparas.</span><span class="sxs-lookup"><span data-stu-id="d3293-110">The security compliance is calculated every day and the history is saved.</span></span>

## <span data-ttu-id="d3293-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3293-111">EXAMPLES</span></span>

### <span data-ttu-id="d3293-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d3293-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityCompliance


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-19Z
Name                       : 2018-08-19Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 19/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-18Z
Name                       : 2018-08-18Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 18/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-17Z
Name                       : 2018-08-17Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 17/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-16Z
Name                       : 2018-08-16Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 16/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-15Z
Name                       : 2018-08-15Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 15/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-14Z
Name                       : 2018-08-14Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 14/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-13Z
Name                       : 2018-08-13Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 13/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-12Z
Name                       : 2018-08-12Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 12/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-11Z
Name                       : 2018-08-11Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 11/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-10Z
Name                       : 2018-08-10Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 10/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-09Z
Name                       : 2018-08-09Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 09/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-08Z
Name                       : 2018-08-08Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 08/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-07Z
Name                       : 2018-08-07Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 07/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="d3293-113">Får ett abonnemangs säkerhets krav för de senaste 14 dagarna</span><span class="sxs-lookup"><span data-stu-id="d3293-113">Gets the security compliance of a subscription for the last 14 days</span></span>

### <span data-ttu-id="d3293-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d3293-114">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityCompliance -Name "2018-08-20Z"


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="d3293-115">Hämtar ett abonnemangs säkerhets krav för ett visst datum</span><span class="sxs-lookup"><span data-stu-id="d3293-115">Gets the security compliance of a subscription on a specific date</span></span>

## <span data-ttu-id="d3293-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3293-116">PARAMETERS</span></span>

### <span data-ttu-id="d3293-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3293-117">-DefaultProfile</span></span>
<span data-ttu-id="d3293-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3293-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3293-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3293-119">-Name</span></span>
<span data-ttu-id="d3293-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d3293-120">Resource name.</span></span>

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

### <span data-ttu-id="d3293-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3293-121">-ResourceId</span></span>
<span data-ttu-id="d3293-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d3293-122">Resource ID.</span></span>

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

### <span data-ttu-id="d3293-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3293-123">CommonParameters</span></span>
<span data-ttu-id="d3293-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3293-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3293-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3293-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3293-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3293-126">INPUTS</span></span>

### <span data-ttu-id="d3293-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d3293-127">System.String</span></span>

## <span data-ttu-id="d3293-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3293-128">OUTPUTS</span></span>

### <span data-ttu-id="d3293-129">Microsoft. Azure. kommandon. Security. Models. efterföljare. PSSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="d3293-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span></span>

## <span data-ttu-id="d3293-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3293-130">NOTES</span></span>

## <span data-ttu-id="d3293-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3293-131">RELATED LINKS</span></span>
