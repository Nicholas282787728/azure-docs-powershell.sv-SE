---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099164"
---
# <span data-ttu-id="65c24-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c24-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="65c24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65c24-102">SYNOPSIS</span></span>

<span data-ttu-id="65c24-103">Skapar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="65c24-103">Creates a runbook.</span></span>

## <span data-ttu-id="65c24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65c24-104">SYNTAX</span></span>

### <span data-ttu-id="65c24-105">ByRunbookName (standard)</span><span class="sxs-lookup"><span data-stu-id="65c24-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="65c24-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="65c24-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65c24-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65c24-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="65c24-108">Cmdleten **New-AzureAutomationRunbook** skapar en ny, Tom Microsoft Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="65c24-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="65c24-109">Ange ett namn för att skapa en ny Runbook.</span><span class="sxs-lookup"><span data-stu-id="65c24-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="65c24-110">Du kan också ange sökvägen till en Windows PowerShell-skriptfil (. ps1) för att importera en Runbook.</span><span class="sxs-lookup"><span data-stu-id="65c24-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="65c24-111">Skriptet som ska importeras måste innehålla en enkel Windows PowerShell-arbetsflöde.</span><span class="sxs-lookup"><span data-stu-id="65c24-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="65c24-112">Namnet på den här Windows PowerShell-arbetsflödet blir namnet på runbooken.</span><span class="sxs-lookup"><span data-stu-id="65c24-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="65c24-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65c24-113">EXAMPLES</span></span>

### <span data-ttu-id="65c24-114">Exempel 1: skapa en Runbook</span><span class="sxs-lookup"><span data-stu-id="65c24-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="65c24-115">Det här kommandot skapar en ny Runbook med namnet Runbook02 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="65c24-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="65c24-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65c24-116">PARAMETERS</span></span>

### <span data-ttu-id="65c24-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65c24-117">-AutomationAccountName</span></span>
<span data-ttu-id="65c24-118">Anger namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="65c24-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="65c24-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="65c24-119">-Description</span></span>
<span data-ttu-id="65c24-120">Anger en beskrivning av Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="65c24-120">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c24-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="65c24-121">-Name</span></span>
<span data-ttu-id="65c24-122">Anger namnet på Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="65c24-122">Specifies the name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c24-123">-Path</span><span class="sxs-lookup"><span data-stu-id="65c24-123">-Path</span></span>
<span data-ttu-id="65c24-124">Anger sökvägen.</span><span class="sxs-lookup"><span data-stu-id="65c24-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c24-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="65c24-125">-Profile</span></span>
<span data-ttu-id="65c24-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="65c24-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65c24-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="65c24-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65c24-128">-Taggar</span><span class="sxs-lookup"><span data-stu-id="65c24-128">-Tags</span></span>
<span data-ttu-id="65c24-129">Anger taggar för Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="65c24-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c24-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c24-130">CommonParameters</span></span>
<span data-ttu-id="65c24-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65c24-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c24-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c24-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c24-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65c24-133">INPUTS</span></span>

## <span data-ttu-id="65c24-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65c24-134">OUTPUTS</span></span>

### <span data-ttu-id="65c24-135">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="65c24-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="65c24-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65c24-136">NOTES</span></span>

## <span data-ttu-id="65c24-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65c24-137">RELATED LINKS</span></span>

[<span data-ttu-id="65c24-138">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c24-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="65c24-139">Publicera – AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c24-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="65c24-140">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c24-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="65c24-141">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c24-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="65c24-142">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c24-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


