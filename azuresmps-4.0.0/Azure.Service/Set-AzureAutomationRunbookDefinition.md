---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099300"
---
# <span data-ttu-id="09cf9-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="09cf9-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="09cf9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09cf9-102">SYNOPSIS</span></span>

<span data-ttu-id="09cf9-103">Uppdaterar utkast definitionen för en Runbook.</span><span class="sxs-lookup"><span data-stu-id="09cf9-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="09cf9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09cf9-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="09cf9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09cf9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="09cf9-106">Cmdleten **set-AzureAutomationRunbookDefinition** uppdaterar utkasts definitionen för en Microsoft Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="09cf9-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="09cf9-107">Ange en Windows PowerShell-skriptfil (. ps1) som innehåller en Runbook som blir utkast till en Runbook.</span><span class="sxs-lookup"><span data-stu-id="09cf9-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="09cf9-108">Om det redan finns en utkast definition kan du använda parametern *Overwrite* för att tvinga cmdleten att skriva över det befintliga utkastet.</span><span class="sxs-lookup"><span data-stu-id="09cf9-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="09cf9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09cf9-109">EXAMPLES</span></span>

### <span data-ttu-id="09cf9-110">Exempel 1: Skriv över ett befintligt utkast till en Runbook</span><span class="sxs-lookup"><span data-stu-id="09cf9-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="09cf9-111">Med det här kommandot skrivs den befintliga utkasts definitionen för en Runbook över.</span><span class="sxs-lookup"><span data-stu-id="09cf9-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="09cf9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09cf9-112">PARAMETERS</span></span>

### <span data-ttu-id="09cf9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="09cf9-113">-AutomationAccountName</span></span>
<span data-ttu-id="09cf9-114">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="09cf9-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="09cf9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="09cf9-115">-Name</span></span>
<span data-ttu-id="09cf9-116">Anger ett namn.</span><span class="sxs-lookup"><span data-stu-id="09cf9-116">Specifies a name.</span></span>

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

### <span data-ttu-id="09cf9-117">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="09cf9-117">-Overwrite</span></span>
<span data-ttu-id="09cf9-118">Anger om ett befintligt utkast ska skrivas över.</span><span class="sxs-lookup"><span data-stu-id="09cf9-118">Indicates whether to overwrite an existing draft definition.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf9-119">-Path</span><span class="sxs-lookup"><span data-stu-id="09cf9-119">-Path</span></span>
<span data-ttu-id="09cf9-120">Anger sökvägen till en Runbook.</span><span class="sxs-lookup"><span data-stu-id="09cf9-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09cf9-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="09cf9-121">-Profile</span></span>
<span data-ttu-id="09cf9-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="09cf9-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="09cf9-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="09cf9-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="09cf9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09cf9-124">CommonParameters</span></span>
<span data-ttu-id="09cf9-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09cf9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09cf9-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09cf9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09cf9-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09cf9-127">INPUTS</span></span>

## <span data-ttu-id="09cf9-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09cf9-128">OUTPUTS</span></span>

### <span data-ttu-id="09cf9-129">Microsoft. Azure. commands. Automation. Model. RunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="09cf9-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="09cf9-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09cf9-130">NOTES</span></span>

## <span data-ttu-id="09cf9-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09cf9-131">RELATED LINKS</span></span>

[<span data-ttu-id="09cf9-132">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="09cf9-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


