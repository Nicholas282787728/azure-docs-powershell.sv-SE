---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101988"
---
# <span data-ttu-id="a07d6-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a07d6-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="a07d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a07d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a07d6-103">Hämtar säkerhets utvärderingar och deras resultat för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="a07d6-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="a07d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a07d6-104">SYNTAX</span></span>

### <span data-ttu-id="a07d6-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="a07d6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a07d6-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a07d6-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a07d6-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="a07d6-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a07d6-108">ID</span><span class="sxs-lookup"><span data-stu-id="a07d6-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a07d6-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a07d6-109">DESCRIPTION</span></span>
<span data-ttu-id="a07d6-110">Hämtar en säkerhets utvärdering och deras resultat för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a07d6-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="a07d6-111">Säkerhets utvärderingar gör att du kan se vilken metod som rekommenderas för Azure-prenumerationen genom att logga in i Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="a07d6-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="a07d6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a07d6-112">EXAMPLES</span></span>

### <span data-ttu-id="a07d6-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a07d6-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="a07d6-114">Får all säkerhets utvärdering i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="a07d6-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="a07d6-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a07d6-115">PARAMETERS</span></span>

### <span data-ttu-id="a07d6-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="a07d6-116">-AssessedResourceId</span></span>
<span data-ttu-id="a07d6-117">Fullständig resurs-ID för resursen som utvärderingen beräknas på.</span><span class="sxs-lookup"><span data-stu-id="a07d6-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a07d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07d6-118">-DefaultProfile</span></span>
<span data-ttu-id="a07d6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a07d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a07d6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a07d6-120">-Name</span></span>
<span data-ttu-id="a07d6-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a07d6-121">Resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07d6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a07d6-122">-ResourceId</span></span>
<span data-ttu-id="a07d6-123">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="a07d6-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a07d6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07d6-124">CommonParameters</span></span>
<span data-ttu-id="a07d6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07d6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07d6-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a07d6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07d6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a07d6-127">INPUTS</span></span>

### <span data-ttu-id="a07d6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a07d6-128">System.String</span></span>

## <span data-ttu-id="a07d6-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a07d6-129">OUTPUTS</span></span>

### <span data-ttu-id="a07d6-130">Microsoft. Azure. kommandon. Security. Models. bedömningar. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="a07d6-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="a07d6-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a07d6-131">NOTES</span></span>

## <span data-ttu-id="a07d6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a07d6-132">RELATED LINKS</span></span>
