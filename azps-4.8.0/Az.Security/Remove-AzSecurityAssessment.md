---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261696"
---
# <span data-ttu-id="06b0c-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="06b0c-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="06b0c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="06b0c-103">Tar bort en säkerhets utvärdering från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="06b0c-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="06b0c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06b0c-104">SYNTAX</span></span>

### <span data-ttu-id="06b0c-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="06b0c-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b0c-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="06b0c-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b0c-107">ID</span><span class="sxs-lookup"><span data-stu-id="06b0c-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b0c-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="06b0c-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06b0c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06b0c-109">DESCRIPTION</span></span>
<span data-ttu-id="06b0c-110">Tar bort ett resultat för säkerhets utvärdering från ett abonnemang, som vanligt vis används när en resoruce tas bort eller när utvärderingen inte är relevant för en viss resurs längre</span><span class="sxs-lookup"><span data-stu-id="06b0c-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="06b0c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06b0c-111">EXAMPLES</span></span>

### <span data-ttu-id="06b0c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06b0c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="06b0c-113">Tar bort ett utvärderings resultat för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="06b0c-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="06b0c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06b0c-114">PARAMETERS</span></span>

### <span data-ttu-id="06b0c-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="06b0c-115">-AssessedResourceId</span></span>
<span data-ttu-id="06b0c-116">Fullständig resurs-ID för resursen som utvärderingen beräknas på.</span><span class="sxs-lookup"><span data-stu-id="06b0c-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b0c-117">-DefaultProfile</span></span>
<span data-ttu-id="06b0c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06b0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06b0c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06b0c-119">-InputObject</span></span>
<span data-ttu-id="06b0c-120">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="06b0c-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06b0c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="06b0c-121">-Name</span></span>
<span data-ttu-id="06b0c-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="06b0c-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b0c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06b0c-123">-PassThru</span></span>
<span data-ttu-id="06b0c-124">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="06b0c-124">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b0c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06b0c-125">-ResourceId</span></span>
<span data-ttu-id="06b0c-126">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="06b0c-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="06b0c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06b0c-127">-Confirm</span></span>
<span data-ttu-id="06b0c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06b0c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b0c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b0c-129">-WhatIf</span></span>
<span data-ttu-id="06b0c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06b0c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b0c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06b0c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b0c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b0c-132">CommonParameters</span></span>
<span data-ttu-id="06b0c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06b0c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b0c-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06b0c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b0c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06b0c-135">INPUTS</span></span>

### <span data-ttu-id="06b0c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="06b0c-136">System.String</span></span>

### <span data-ttu-id="06b0c-137">Microsoft. Azure. kommandon. Security. Models. bedömningar. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="06b0c-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="06b0c-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06b0c-138">OUTPUTS</span></span>

### <span data-ttu-id="06b0c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06b0c-139">System.Boolean</span></span>

## <span data-ttu-id="06b0c-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06b0c-140">NOTES</span></span>

## <span data-ttu-id="06b0c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06b0c-141">RELATED LINKS</span></span>
