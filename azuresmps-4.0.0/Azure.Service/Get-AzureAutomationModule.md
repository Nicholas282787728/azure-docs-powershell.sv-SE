---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099598"
---
# <span data-ttu-id="11e12-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="11e12-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="11e12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11e12-102">SYNOPSIS</span></span>

<span data-ttu-id="11e12-103">Skaffa en Azure Automation-modul.</span><span class="sxs-lookup"><span data-stu-id="11e12-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="11e12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11e12-104">SYNTAX</span></span>

### <span data-ttu-id="11e12-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="11e12-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="11e12-106">ByName</span><span class="sxs-lookup"><span data-stu-id="11e12-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="11e12-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11e12-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="11e12-108">Cmdleten **Get-AzureAutomationModule** hämtar en eller flera Microsoft Azure Automation-moduler.</span><span class="sxs-lookup"><span data-stu-id="11e12-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="11e12-109">Alla moduler returneras som standard.</span><span class="sxs-lookup"><span data-stu-id="11e12-109">By default, all modules are returned.</span></span>
<span data-ttu-id="11e12-110">Om du vill hämta en specifik modul anger du dess namn.</span><span class="sxs-lookup"><span data-stu-id="11e12-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="11e12-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11e12-111">EXAMPLES</span></span>

### <span data-ttu-id="11e12-112">Exempel 1: Hämta alla moduler</span><span class="sxs-lookup"><span data-stu-id="11e12-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="11e12-113">Det här kommandot får alla moduler i Azure Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="11e12-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="11e12-114">Exempel 2: Hämta en modul</span><span class="sxs-lookup"><span data-stu-id="11e12-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="11e12-115">Det här kommandot hämtar en modul som heter ContosoModule i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="11e12-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="11e12-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11e12-116">PARAMETERS</span></span>

### <span data-ttu-id="11e12-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11e12-117">-AutomationAccountName</span></span>
<span data-ttu-id="11e12-118">Anger namnet på Automation-kontot där Runbook ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="11e12-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

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

### <span data-ttu-id="11e12-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="11e12-119">-Name</span></span>
<span data-ttu-id="11e12-120">Anger namnet på en modul som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="11e12-120">Specifies the name of a module to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e12-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="11e12-121">-Profile</span></span>
<span data-ttu-id="11e12-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="11e12-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11e12-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="11e12-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11e12-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e12-124">CommonParameters</span></span>
<span data-ttu-id="11e12-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e12-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e12-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e12-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e12-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11e12-127">INPUTS</span></span>

## <span data-ttu-id="11e12-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11e12-128">OUTPUTS</span></span>

### <span data-ttu-id="11e12-129">Microsoft. Azure. commands. Automation. Model. modul</span><span class="sxs-lookup"><span data-stu-id="11e12-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="11e12-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11e12-130">NOTES</span></span>

## <span data-ttu-id="11e12-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11e12-131">RELATED LINKS</span></span>

[<span data-ttu-id="11e12-132">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="11e12-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="11e12-133">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="11e12-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="11e12-134">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="11e12-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


