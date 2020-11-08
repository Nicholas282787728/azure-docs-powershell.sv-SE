---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099711"
---
# <span data-ttu-id="f5ae1-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f5ae1-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="f5ae1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5ae1-102">SYNOPSIS</span></span>

<span data-ttu-id="f5ae1-103">Tar bort en modul från Automation.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="f5ae1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5ae1-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f5ae1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5ae1-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f5ae1-106">Cmdleten **Remove-AzureAutomationModule** tar bort ett Automation-konto från Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="f5ae1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5ae1-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ae1-108">Exempel 1: ta bort en modul</span><span class="sxs-lookup"><span data-stu-id="f5ae1-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="f5ae1-109">Det här kommandot tar bort en modul som heter ContosoModule från Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f5ae1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5ae1-110">PARAMETERS</span></span>

### <span data-ttu-id="f5ae1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f5ae1-111">-AutomationAccountName</span></span>
<span data-ttu-id="f5ae1-112">Anger namnet på Automation-kontot med modulen.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="f5ae1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f5ae1-113">-Force</span></span>
<span data-ttu-id="f5ae1-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5ae1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5ae1-115">-Name</span></span>
<span data-ttu-id="f5ae1-116">Anger namnet på den modul som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="f5ae1-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="f5ae1-117">-Profile</span></span>
<span data-ttu-id="f5ae1-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5ae1-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5ae1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ae1-120">CommonParameters</span></span>
<span data-ttu-id="f5ae1-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ae1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ae1-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5ae1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ae1-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5ae1-123">INPUTS</span></span>

## <span data-ttu-id="f5ae1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5ae1-124">OUTPUTS</span></span>

## <span data-ttu-id="f5ae1-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5ae1-125">NOTES</span></span>

## <span data-ttu-id="f5ae1-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5ae1-126">RELATED LINKS</span></span>

[<span data-ttu-id="f5ae1-127">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f5ae1-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="f5ae1-128">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f5ae1-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="f5ae1-129">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f5ae1-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


