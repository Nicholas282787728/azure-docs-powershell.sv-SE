---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099592"
---
# <span data-ttu-id="e6026-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="e6026-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="e6026-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6026-102">SYNOPSIS</span></span>

<span data-ttu-id="e6026-103">Hämtar en Runbook-definition.</span><span class="sxs-lookup"><span data-stu-id="e6026-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="e6026-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6026-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6026-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6026-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e6026-106">Cmdleten **Get-AzureAutomationRunbookDefinition** hämtar utkast definitionen, den publicerade definitionen eller båda definitionerna av en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="e6026-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="e6026-107">Den publicerade versionen returneras som standard.</span><span class="sxs-lookup"><span data-stu-id="e6026-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="e6026-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6026-108">EXAMPLES</span></span>

### <span data-ttu-id="e6026-109">Exempel 1: Hämta en Runbook-definition</span><span class="sxs-lookup"><span data-stu-id="e6026-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="e6026-110">Det här kommandot hämtar Runbook-definitionen för Runbook-flödet som heter RunbookDef01 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e6026-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e6026-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6026-111">PARAMETERS</span></span>

### <span data-ttu-id="e6026-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e6026-112">-AutomationAccountName</span></span>
<span data-ttu-id="e6026-113">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="e6026-113">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6026-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6026-114">-Name</span></span>
<span data-ttu-id="e6026-115">Anger namnet på en Runbook.</span><span class="sxs-lookup"><span data-stu-id="e6026-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6026-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="e6026-116">-Profile</span></span>
<span data-ttu-id="e6026-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e6026-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6026-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e6026-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6026-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="e6026-119">-Slot</span></span>
<span data-ttu-id="e6026-120">Anger platsen.</span><span class="sxs-lookup"><span data-stu-id="e6026-120">Specifies the slot.</span></span>
<span data-ttu-id="e6026-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e6026-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6026-122">Runbook</span><span class="sxs-lookup"><span data-stu-id="e6026-122">Draft</span></span>
- <span data-ttu-id="e6026-123">Opublicera</span><span class="sxs-lookup"><span data-stu-id="e6026-123">Published</span></span>

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

### <span data-ttu-id="e6026-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6026-124">CommonParameters</span></span>
<span data-ttu-id="e6026-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6026-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6026-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6026-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6026-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6026-127">INPUTS</span></span>

## <span data-ttu-id="e6026-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6026-128">OUTPUTS</span></span>

## <span data-ttu-id="e6026-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6026-129">NOTES</span></span>

## <span data-ttu-id="e6026-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6026-130">RELATED LINKS</span></span>

[<span data-ttu-id="e6026-131">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="e6026-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


