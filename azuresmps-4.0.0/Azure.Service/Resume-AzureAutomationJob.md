---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093188"
---
# <span data-ttu-id="0cd08-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0cd08-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="0cd08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cd08-102">SYNOPSIS</span></span>

<span data-ttu-id="0cd08-103">Återupptar ett uppehållet automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="0cd08-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="0cd08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cd08-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cd08-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cd08-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0cd08-106">Cmdleten **Resume-AzureAutomationJob** fortsätter att ha stoppat Microsoft Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="0cd08-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="0cd08-107">Använd parametern *ID* för att ange det upphävda jobbet.</span><span class="sxs-lookup"><span data-stu-id="0cd08-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="0cd08-108">Om du vill pausa ett jobb kan du använda Suspend-AzureAutomationJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cd08-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="0cd08-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cd08-109">EXAMPLES</span></span>

### <span data-ttu-id="0cd08-110">Exempel 1: återuppta ett avbrutet jobb</span><span class="sxs-lookup"><span data-stu-id="0cd08-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="0cd08-111">Det här kommandot återupptar jobbet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="0cd08-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="0cd08-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cd08-112">PARAMETERS</span></span>

### <span data-ttu-id="0cd08-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0cd08-113">-AutomationAccountName</span></span>
<span data-ttu-id="0cd08-114">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="0cd08-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="0cd08-115">-ID</span><span class="sxs-lookup"><span data-stu-id="0cd08-115">-Id</span></span>
<span data-ttu-id="0cd08-116">Anger ID för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="0cd08-116">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd08-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="0cd08-117">-Profile</span></span>
<span data-ttu-id="0cd08-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0cd08-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0cd08-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0cd08-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0cd08-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd08-120">CommonParameters</span></span>
<span data-ttu-id="0cd08-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd08-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd08-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd08-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd08-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cd08-123">INPUTS</span></span>

## <span data-ttu-id="0cd08-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cd08-124">OUTPUTS</span></span>

## <span data-ttu-id="0cd08-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cd08-125">NOTES</span></span>

## <span data-ttu-id="0cd08-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cd08-126">RELATED LINKS</span></span>

[<span data-ttu-id="0cd08-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0cd08-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="0cd08-128">Stopp-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0cd08-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="0cd08-129">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0cd08-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


