---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CE04DEE6-28AE-43A3-A8DE-98AC0A57E575
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1c2d9a3aa53cb8efd2924f24aa80db2c7fd07fea
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093485"
---
# <span data-ttu-id="5fe8a-101">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5fe8a-101">Suspend-AzureAutomationJob</span></span>

## <span data-ttu-id="5fe8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fe8a-102">SYNOPSIS</span></span>

<span data-ttu-id="5fe8a-103">Inaktiverar ett automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="5fe8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fe8a-104">SYNTAX</span></span>

```
Suspend-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fe8a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fe8a-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5fe8a-106">Cmdleten **suspend-AzureAutomationJob** avbryter ett Microsoft Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-106">The **Suspend-AzureAutomationJob** cmdlet suspends a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="5fe8a-107">Ange ett automatiserings jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-107">Specify a running Automation job.</span></span>

<span data-ttu-id="5fe8a-108">Om du vill återuppta ett avbrutet jobb använder du cmdleten **Resume-AzureAutomationJob** .</span><span class="sxs-lookup"><span data-stu-id="5fe8a-108">To resume a suspended job, use the **Resume-AzureAutomationJob** cmdlet.</span></span>

## <span data-ttu-id="5fe8a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fe8a-109">EXAMPLES</span></span>

### <span data-ttu-id="5fe8a-110">Exempel 1: pausa ett jobb</span><span class="sxs-lookup"><span data-stu-id="5fe8a-110">Example 1: Suspend a job</span></span>
```
PS C:\> Suspend-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="5fe8a-111">Det här kommandot avaktiverar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="5fe8a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fe8a-112">PARAMETERS</span></span>

### <span data-ttu-id="5fe8a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5fe8a-113">-AutomationAccountName</span></span>
<span data-ttu-id="5fe8a-114">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="5fe8a-115">-ID</span><span class="sxs-lookup"><span data-stu-id="5fe8a-115">-Id</span></span>
<span data-ttu-id="5fe8a-116">Anger ID för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="5fe8a-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="5fe8a-117">-Profile</span></span>
<span data-ttu-id="5fe8a-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5fe8a-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5fe8a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe8a-120">CommonParameters</span></span>
<span data-ttu-id="5fe8a-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe8a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe8a-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe8a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe8a-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fe8a-123">INPUTS</span></span>

## <span data-ttu-id="5fe8a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fe8a-124">OUTPUTS</span></span>

## <span data-ttu-id="5fe8a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fe8a-125">NOTES</span></span>

## <span data-ttu-id="5fe8a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fe8a-126">RELATED LINKS</span></span>

[<span data-ttu-id="5fe8a-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5fe8a-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="5fe8a-128">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5fe8a-128">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="5fe8a-129">Stopp-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5fe8a-129">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)


