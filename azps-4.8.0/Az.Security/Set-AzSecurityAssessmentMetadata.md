---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258610"
---
# <span data-ttu-id="c0d54-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="c0d54-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="c0d54-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0d54-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d54-103">Skapar eller uppdaterar en typ av säkerhets utvärdering.</span><span class="sxs-lookup"><span data-stu-id="c0d54-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="c0d54-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0d54-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d54-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0d54-105">DESCRIPTION</span></span>
<span data-ttu-id="c0d54-106">Skapar eller uppdaterar metadata för en säkerhets utvärdering som kan användas för att skapa och hantera olika utvärderings egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c0d54-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="c0d54-107">Efter den här åtgärden kan du rapportera utvärderings resultat för alla resurser i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c0d54-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="c0d54-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0d54-108">EXAMPLES</span></span>

### <span data-ttu-id="c0d54-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0d54-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="c0d54-110">Skapa en ny utvärderings typ i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c0d54-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="c0d54-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0d54-111">PARAMETERS</span></span>

### <span data-ttu-id="c0d54-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d54-112">-DefaultProfile</span></span>
<span data-ttu-id="c0d54-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d54-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d54-114">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c0d54-114">-Description</span></span>
<span data-ttu-id="c0d54-115">Detaljerad sträng som hjälper användarna att förstå innebörden av denna utvärdering och hur den beräknas.</span><span class="sxs-lookup"><span data-stu-id="c0d54-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d54-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c0d54-116">-DisplayName</span></span>
<span data-ttu-id="c0d54-117">Läsbar rubrik för det här objektet.</span><span class="sxs-lookup"><span data-stu-id="c0d54-117">Human readable title for this object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d54-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0d54-118">-Name</span></span>
<span data-ttu-id="c0d54-119">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c0d54-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d54-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="c0d54-120">-RemediationDescription</span></span>
<span data-ttu-id="c0d54-121">Detaljerad sträng som hjälper användarna att förstå olika sätt att begränsa eller åtgärda säkerhets problemet.</span><span class="sxs-lookup"><span data-stu-id="c0d54-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d54-122">– Allvarlighets grad</span><span class="sxs-lookup"><span data-stu-id="c0d54-122">-Severity</span></span>
<span data-ttu-id="c0d54-123">Anger betydelsen av säkerhets risken om utvärderingen är ohälsosam.</span><span class="sxs-lookup"><span data-stu-id="c0d54-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d54-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0d54-124">-Confirm</span></span>
<span data-ttu-id="c0d54-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0d54-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d54-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d54-126">-WhatIf</span></span>
<span data-ttu-id="c0d54-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0d54-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0d54-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0d54-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d54-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d54-129">CommonParameters</span></span>
<span data-ttu-id="c0d54-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0d54-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d54-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0d54-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d54-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0d54-132">INPUTS</span></span>

### <span data-ttu-id="c0d54-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="c0d54-133">None</span></span>

## <span data-ttu-id="c0d54-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0d54-134">OUTPUTS</span></span>

### <span data-ttu-id="c0d54-135">Microsoft. Azure. commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="c0d54-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="c0d54-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0d54-136">NOTES</span></span>

## <span data-ttu-id="c0d54-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0d54-137">RELATED LINKS</span></span>
