---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388128"
---
# <span data-ttu-id="1426c-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="1426c-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="1426c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1426c-102">SYNOPSIS</span></span>
<span data-ttu-id="1426c-103">Hämtar säkerhets utvärderings typer och metadta i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="1426c-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="1426c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1426c-104">SYNTAX</span></span>

### <span data-ttu-id="1426c-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="1426c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1426c-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="1426c-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1426c-107">ID</span><span class="sxs-lookup"><span data-stu-id="1426c-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1426c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1426c-108">DESCRIPTION</span></span>
<span data-ttu-id="1426c-109">Hämtar säkerhets utvärderings typer och metadta i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="1426c-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="1426c-110">Metadata för säkerhets utvärdering inkluderar Built-In utvärderingar och anpassade utvärderings typer som användaren kan definiera.</span><span class="sxs-lookup"><span data-stu-id="1426c-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="1426c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1426c-111">EXAMPLES</span></span>

### <span data-ttu-id="1426c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1426c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="1426c-113">Får alla inbyggda bedömningar och anpassade utvärderingar som har kon figurer ATS för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1426c-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="1426c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1426c-114">PARAMETERS</span></span>

### <span data-ttu-id="1426c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1426c-115">-DefaultProfile</span></span>
<span data-ttu-id="1426c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1426c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1426c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1426c-117">-Name</span></span>
<span data-ttu-id="1426c-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="1426c-118">Resource name.</span></span>

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

### <span data-ttu-id="1426c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1426c-119">-ResourceId</span></span>
<span data-ttu-id="1426c-120">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="1426c-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="1426c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1426c-121">CommonParameters</span></span>
<span data-ttu-id="1426c-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1426c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1426c-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1426c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1426c-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1426c-124">INPUTS</span></span>

### <span data-ttu-id="1426c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1426c-125">System.String</span></span>

## <span data-ttu-id="1426c-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1426c-126">OUTPUTS</span></span>

### <span data-ttu-id="1426c-127">Microsoft. Azure. commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="1426c-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="1426c-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1426c-128">NOTES</span></span>

## <span data-ttu-id="1426c-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1426c-129">RELATED LINKS</span></span>
