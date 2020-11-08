---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093384"
---
# <span data-ttu-id="1b18e-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1b18e-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="1b18e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b18e-102">SYNOPSIS</span></span>

<span data-ttu-id="1b18e-103">Hämtar utdata från ett Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="1b18e-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="1b18e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b18e-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1b18e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b18e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1b18e-106">Cmdleten **Get-AzureAutomationJobOutput** hämtar utdata från ett Microsoft Azure Automation-jobb.</span><span class="sxs-lookup"><span data-stu-id="1b18e-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="1b18e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b18e-107">EXAMPLES</span></span>

### <span data-ttu-id="1b18e-108">Exempel 1: få utdata från ett Azure Automation-jobb</span><span class="sxs-lookup"><span data-stu-id="1b18e-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="1b18e-109">Det här kommandot får alla utdata från jobbet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="1b18e-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="1b18e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b18e-110">PARAMETERS</span></span>

### <span data-ttu-id="1b18e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1b18e-111">-AutomationAccountName</span></span>
<span data-ttu-id="1b18e-112">Anger namnet på ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="1b18e-112">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="1b18e-113">-ID</span><span class="sxs-lookup"><span data-stu-id="1b18e-113">-Id</span></span>
<span data-ttu-id="1b18e-114">Anger ID för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="1b18e-114">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="1b18e-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="1b18e-115">-Profile</span></span>
<span data-ttu-id="1b18e-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1b18e-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1b18e-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1b18e-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1b18e-118">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1b18e-118">-StartTime</span></span>
<span data-ttu-id="1b18e-119">Anger en start tid.</span><span class="sxs-lookup"><span data-stu-id="1b18e-119">Specifies a start time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b18e-120">-Stream</span><span class="sxs-lookup"><span data-stu-id="1b18e-120">-Stream</span></span>
<span data-ttu-id="1b18e-121">Anger typen av utdata.</span><span class="sxs-lookup"><span data-stu-id="1b18e-121">Specifies the type of output.</span></span>
<span data-ttu-id="1b18e-122">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="1b18e-122">Valid values are:</span></span> 

- <span data-ttu-id="1b18e-123">Eventuell</span><span class="sxs-lookup"><span data-stu-id="1b18e-123">Any</span></span>
- <span data-ttu-id="1b18e-124">Verk</span><span class="sxs-lookup"><span data-stu-id="1b18e-124">Debug</span></span>
- <span data-ttu-id="1b18e-125">Synkroniseringsfel</span><span class="sxs-lookup"><span data-stu-id="1b18e-125">Error</span></span>
- <span data-ttu-id="1b18e-126">Skriva</span><span class="sxs-lookup"><span data-stu-id="1b18e-126">Output</span></span>
- <span data-ttu-id="1b18e-127">Status</span><span class="sxs-lookup"><span data-stu-id="1b18e-127">Progress</span></span>
- <span data-ttu-id="1b18e-128">Utförlig</span><span class="sxs-lookup"><span data-stu-id="1b18e-128">Verbose</span></span>
- <span data-ttu-id="1b18e-129">Meddelandet</span><span class="sxs-lookup"><span data-stu-id="1b18e-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b18e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b18e-130">CommonParameters</span></span>
<span data-ttu-id="1b18e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b18e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b18e-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b18e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b18e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b18e-133">INPUTS</span></span>

## <span data-ttu-id="1b18e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b18e-134">OUTPUTS</span></span>

## <span data-ttu-id="1b18e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b18e-135">NOTES</span></span>

## <span data-ttu-id="1b18e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b18e-136">RELATED LINKS</span></span>

[<span data-ttu-id="1b18e-137">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1b18e-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="1b18e-138">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1b18e-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="1b18e-139">Stopp-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1b18e-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="1b18e-140">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1b18e-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


