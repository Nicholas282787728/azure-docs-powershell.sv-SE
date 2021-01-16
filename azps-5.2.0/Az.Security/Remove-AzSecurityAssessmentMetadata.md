---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391459"
---
# <span data-ttu-id="94e68-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="94e68-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="94e68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94e68-102">SYNOPSIS</span></span>
<span data-ttu-id="94e68-103">Tar bort en metadata för säkerhets utvärdering från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="94e68-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="94e68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94e68-104">SYNTAX</span></span>

### <span data-ttu-id="94e68-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="94e68-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e68-106">ID</span><span class="sxs-lookup"><span data-stu-id="94e68-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e68-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="94e68-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94e68-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94e68-108">DESCRIPTION</span></span>
<span data-ttu-id="94e68-109">Tar bort en metadata för säkerhets utvärdering från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="94e68-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="94e68-110">Den här åtgärden tar bort utvärderings typen och alla relevanta utvärderings resultat från abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="94e68-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="94e68-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94e68-111">EXAMPLES</span></span>

### <span data-ttu-id="94e68-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="94e68-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="94e68-113">Tar bort en utvärderings typ från ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="94e68-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="94e68-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94e68-114">PARAMETERS</span></span>

### <span data-ttu-id="94e68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e68-115">-DefaultProfile</span></span>
<span data-ttu-id="94e68-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94e68-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94e68-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94e68-117">-InputObject</span></span>
<span data-ttu-id="94e68-118">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="94e68-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94e68-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="94e68-119">-Name</span></span>
<span data-ttu-id="94e68-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="94e68-120">Resource name.</span></span>

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

### <span data-ttu-id="94e68-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94e68-121">-PassThru</span></span>
<span data-ttu-id="94e68-122">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="94e68-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="94e68-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94e68-123">-ResourceId</span></span>
<span data-ttu-id="94e68-124">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="94e68-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="94e68-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94e68-125">-Confirm</span></span>
<span data-ttu-id="94e68-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94e68-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e68-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e68-127">-WhatIf</span></span>
<span data-ttu-id="94e68-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94e68-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e68-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94e68-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e68-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e68-130">CommonParameters</span></span>
<span data-ttu-id="94e68-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94e68-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e68-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94e68-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e68-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94e68-133">INPUTS</span></span>

### <span data-ttu-id="94e68-134">System. String</span><span class="sxs-lookup"><span data-stu-id="94e68-134">System.String</span></span>

### <span data-ttu-id="94e68-135">Microsoft. Azure. commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="94e68-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="94e68-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94e68-136">OUTPUTS</span></span>

### <span data-ttu-id="94e68-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94e68-137">System.Boolean</span></span>

## <span data-ttu-id="94e68-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94e68-138">NOTES</span></span>

## <span data-ttu-id="94e68-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94e68-139">RELATED LINKS</span></span>
