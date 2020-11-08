---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: EA7C1449-E11F-4AE8-A513-59BDCA38875D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e432edd2469fa25519c12f0cd1f2dadb1d0dca2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099817"
---
# <span data-ttu-id="af7cb-101">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="af7cb-101">Unregister-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="af7cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af7cb-102">SYNOPSIS</span></span>

<span data-ttu-id="af7cb-103">Tar bort en association mellan en Runbook och ett schema.</span><span class="sxs-lookup"><span data-stu-id="af7cb-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="af7cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af7cb-104">SYNTAX</span></span>

### <span data-ttu-id="af7cb-105">ByJobScheduleId (standard)</span><span class="sxs-lookup"><span data-stu-id="af7cb-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="af7cb-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="af7cb-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="af7cb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af7cb-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="af7cb-108">Med cmdleten **Unregistered-AzureAutomationScheduledRunbook** tar du bort associationen mellan en Microsoft Azure Automation-Runbook och ett schema, som hindrar Runbook-flödet från att starta när schemat utlöses.</span><span class="sxs-lookup"><span data-stu-id="af7cb-108">The **Unregister-AzureAutomationScheduledRunbook** cmdlet removes the association between a Microsoft Azure Automation runbook and a schedule, which stops the runbook from starting when the schedule fires.</span></span>

## <span data-ttu-id="af7cb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af7cb-109">EXAMPLES</span></span>

### <span data-ttu-id="af7cb-110">Exempel 1: ta bort kopplingen mellan en Runbook och ett schema</span><span class="sxs-lookup"><span data-stu-id="af7cb-110">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\> Unregister-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="af7cb-111">Det här kommandot tar bort associationen mellan Runbook-flödet med namnet Runbk01 och schemat med namnet Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="af7cb-111">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="af7cb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af7cb-112">PARAMETERS</span></span>

### <span data-ttu-id="af7cb-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="af7cb-113">-AutomationAccountName</span></span>
<span data-ttu-id="af7cb-114">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="af7cb-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="af7cb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="af7cb-115">-Force</span></span>
<span data-ttu-id="af7cb-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="af7cb-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af7cb-117">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="af7cb-117">-JobScheduleId</span></span>
<span data-ttu-id="af7cb-118">Anger ID för en schemalagd Runbook.</span><span class="sxs-lookup"><span data-stu-id="af7cb-118">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af7cb-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="af7cb-119">-Profile</span></span>
<span data-ttu-id="af7cb-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="af7cb-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af7cb-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="af7cb-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="af7cb-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="af7cb-122">-RunbookName</span></span>
<span data-ttu-id="af7cb-123">Anger namnet på en Runbook.</span><span class="sxs-lookup"><span data-stu-id="af7cb-123">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af7cb-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="af7cb-124">-ScheduleName</span></span>
<span data-ttu-id="af7cb-125">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="af7cb-125">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af7cb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7cb-126">CommonParameters</span></span>
<span data-ttu-id="af7cb-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af7cb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7cb-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7cb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7cb-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af7cb-129">INPUTS</span></span>

## <span data-ttu-id="af7cb-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af7cb-130">OUTPUTS</span></span>

## <span data-ttu-id="af7cb-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af7cb-131">NOTES</span></span>

## <span data-ttu-id="af7cb-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af7cb-132">RELATED LINKS</span></span>

[<span data-ttu-id="af7cb-133">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="af7cb-133">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)


