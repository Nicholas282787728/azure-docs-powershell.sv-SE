---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271402"
---
# <span data-ttu-id="3c5fb-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="3c5fb-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="3c5fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="3c5fb-103">Hämtar under bedömningar i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="3c5fb-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="3c5fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c5fb-104">SYNTAX</span></span>

### <span data-ttu-id="3c5fb-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="3c5fb-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c5fb-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3c5fb-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c5fb-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="3c5fb-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c5fb-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="3c5fb-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c5fb-109">ID</span><span class="sxs-lookup"><span data-stu-id="3c5fb-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c5fb-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c5fb-110">DESCRIPTION</span></span>
<span data-ttu-id="3c5fb-111">Hämtar under bedömningar i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="3c5fb-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="3c5fb-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c5fb-112">EXAMPLES</span></span>

### <span data-ttu-id="3c5fb-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3c5fb-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="3c5fb-114">Får alla under bedömningar ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="3c5fb-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="3c5fb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c5fb-115">PARAMETERS</span></span>

### <span data-ttu-id="3c5fb-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="3c5fb-116">-AssessedResourceId</span></span>
<span data-ttu-id="3c5fb-117">Fullständig resurs-ID för resursen som utvärderingen beräknas på.</span><span class="sxs-lookup"><span data-stu-id="3c5fb-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c5fb-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="3c5fb-118">-AssessmentName</span></span>
<span data-ttu-id="3c5fb-119">Namn på utvärderings resursen.</span><span class="sxs-lookup"><span data-stu-id="3c5fb-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c5fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c5fb-120">-DefaultProfile</span></span>
<span data-ttu-id="3c5fb-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c5fb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c5fb-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c5fb-122">-Name</span></span>
<span data-ttu-id="3c5fb-123">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="3c5fb-123">Resource name.</span></span>

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
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c5fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c5fb-124">-ResourceId</span></span>
<span data-ttu-id="3c5fb-125">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="3c5fb-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3c5fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c5fb-126">CommonParameters</span></span>
<span data-ttu-id="3c5fb-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c5fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c5fb-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c5fb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c5fb-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c5fb-129">INPUTS</span></span>

### <span data-ttu-id="3c5fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3c5fb-130">System.String</span></span>

## <span data-ttu-id="3c5fb-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c5fb-131">OUTPUTS</span></span>

### <span data-ttu-id="3c5fb-132">Microsoft. Azure. kommandon. Security. Models. subbedömningar. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="3c5fb-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="3c5fb-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c5fb-133">NOTES</span></span>

## <span data-ttu-id="3c5fb-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c5fb-134">RELATED LINKS</span></span>
