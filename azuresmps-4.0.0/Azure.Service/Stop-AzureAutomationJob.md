---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099172"
---
# <span data-ttu-id="3e9eb-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3e9eb-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="3e9eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e9eb-102">SYNOPSIS</span></span>

<span data-ttu-id="3e9eb-103">Stoppar ett automatiserings jobb.</span><span class="sxs-lookup"><span data-stu-id="3e9eb-103">Stops an Automation job.</span></span>

## <span data-ttu-id="3e9eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e9eb-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e9eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e9eb-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3e9eb-106">Cmdleten **Stop-AzureAutomationJob** stoppar ett Microsoft Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="3e9eb-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="3e9eb-107">Ange ett automatiserings jobb som körs.</span><span class="sxs-lookup"><span data-stu-id="3e9eb-107">Specify a running automation job.</span></span>

## <span data-ttu-id="3e9eb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e9eb-108">EXAMPLES</span></span>

### <span data-ttu-id="3e9eb-109">Exempel 1: stoppa ett jobb</span><span class="sxs-lookup"><span data-stu-id="3e9eb-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="3e9eb-110">Det här kommandot stoppar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="3e9eb-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="3e9eb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e9eb-111">PARAMETERS</span></span>

### <span data-ttu-id="3e9eb-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3e9eb-112">-AutomationAccountName</span></span>
<span data-ttu-id="3e9eb-113">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="3e9eb-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="3e9eb-114">-ID</span><span class="sxs-lookup"><span data-stu-id="3e9eb-114">-Id</span></span>
<span data-ttu-id="3e9eb-115">Anger ID för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="3e9eb-115">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="3e9eb-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="3e9eb-116">-Profile</span></span>
<span data-ttu-id="3e9eb-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3e9eb-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e9eb-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3e9eb-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3e9eb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9eb-119">CommonParameters</span></span>
<span data-ttu-id="3e9eb-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e9eb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9eb-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e9eb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9eb-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e9eb-122">INPUTS</span></span>

## <span data-ttu-id="3e9eb-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e9eb-123">OUTPUTS</span></span>

## <span data-ttu-id="3e9eb-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e9eb-124">NOTES</span></span>

## <span data-ttu-id="3e9eb-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e9eb-125">RELATED LINKS</span></span>

[<span data-ttu-id="3e9eb-126">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3e9eb-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="3e9eb-127">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3e9eb-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="3e9eb-128">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="3e9eb-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


