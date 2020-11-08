---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258607"
---
# <span data-ttu-id="c7c1f-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="c7c1f-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="c7c1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c1f-103">Skapa eller uppdatera ett säkerhets utvärderings resultat för en resurs</span><span class="sxs-lookup"><span data-stu-id="c7c1f-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="c7c1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7c1f-104">SYNTAX</span></span>

### <span data-ttu-id="c7c1f-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="c7c1f-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c1f-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="c7c1f-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7c1f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7c1f-107">DESCRIPTION</span></span>
<span data-ttu-id="c7c1f-108">Skapa eller uppdatera ett säkerhets utvärderings resultat på en resurs kan användas för att ändra status för ett befintligt resultat eller lägga till ytterligare data.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="c7c1f-109">kan endast användas för utvärderings typer för "CustomerManaged" och bara efter att den matchade utvärderings-metadata har skapats.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="c7c1f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7c1f-110">EXAMPLES</span></span>

### <span data-ttu-id="c7c1f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7c1f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="c7c1f-112">Markerar prenumerations resultatet som "ohälsosamt" för utvärdering av typen "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D". mer information om utvärderings typen finns under typen av assessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="c7c1f-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="c7c1f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7c1f-113">PARAMETERS</span></span>

### <span data-ttu-id="c7c1f-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="c7c1f-114">-AdditionalData</span></span>
<span data-ttu-id="c7c1f-115">Data som är kopplade till utvärderings resultatet för bättre undersökningar eller status skärpa.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c1f-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="c7c1f-116">-AssessedResourceId</span></span>
<span data-ttu-id="c7c1f-117">Fullständig resurs-ID för resursen som utvärderingen beräknas på.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="c7c1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c1f-118">-DefaultProfile</span></span>
<span data-ttu-id="c7c1f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c1f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7c1f-120">-Name</span></span>
<span data-ttu-id="c7c1f-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-121">Resource name.</span></span>

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

### <span data-ttu-id="c7c1f-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="c7c1f-122">-StatusCause</span></span>
<span data-ttu-id="c7c1f-123">Progremmatic-kod för orsaken till utvärderings resultatet.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="c7c1f-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="c7c1f-124">-StatusCode</span></span>
<span data-ttu-id="c7c1f-125">Progremmatic-kod för resultatet av utvärderingen.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="c7c1f-126">kan vara "felfri", "ohälsosamt" eller "NotApplicable"</span><span class="sxs-lookup"><span data-stu-id="c7c1f-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
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

### <span data-ttu-id="c7c1f-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="c7c1f-127">-StatusDescription</span></span>
<span data-ttu-id="c7c1f-128">Lättläst Beskrivning av orsaken till utvärderings resultatet.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="c7c1f-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7c1f-129">-Confirm</span></span>
<span data-ttu-id="c7c1f-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7c1f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7c1f-131">-WhatIf</span></span>
<span data-ttu-id="c7c1f-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7c1f-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7c1f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c1f-134">CommonParameters</span></span>
<span data-ttu-id="c7c1f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c1f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c1f-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7c1f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c1f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7c1f-137">INPUTS</span></span>

### <span data-ttu-id="c7c1f-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="c7c1f-138">None</span></span>

## <span data-ttu-id="c7c1f-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7c1f-139">OUTPUTS</span></span>

### <span data-ttu-id="c7c1f-140">Microsoft. Azure. kommandon. Security. Models. bedömningar. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="c7c1f-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="c7c1f-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7c1f-141">NOTES</span></span>

## <span data-ttu-id="c7c1f-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7c1f-142">RELATED LINKS</span></span>
