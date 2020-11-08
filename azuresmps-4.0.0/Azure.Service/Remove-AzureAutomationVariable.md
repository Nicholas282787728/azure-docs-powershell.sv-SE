---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099399"
---
# <span data-ttu-id="5f656-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5f656-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="5f656-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f656-102">SYNOPSIS</span></span>

<span data-ttu-id="5f656-103">Tar bort en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="5f656-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="5f656-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f656-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5f656-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f656-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5f656-106">Cmdleten **Remove-AzureAutomationVariable** tar bort en variabel från Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5f656-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="5f656-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f656-107">EXAMPLES</span></span>

### <span data-ttu-id="5f656-108">Exempel 1: ta bort en variabel</span><span class="sxs-lookup"><span data-stu-id="5f656-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="5f656-109">Det här kommandot tar bort en variabel som heter MyStringVariable i Automation-kontot med namnet Contoso17 utan att fråga efter användar verifiering.</span><span class="sxs-lookup"><span data-stu-id="5f656-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="5f656-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f656-110">PARAMETERS</span></span>

### <span data-ttu-id="5f656-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f656-111">-AutomationAccountName</span></span>
<span data-ttu-id="5f656-112">Anger namnet på Automation-kontot med variabeln.</span><span class="sxs-lookup"><span data-stu-id="5f656-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="5f656-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5f656-113">-Force</span></span>
<span data-ttu-id="5f656-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5f656-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5f656-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f656-115">-Name</span></span>
<span data-ttu-id="5f656-116">Anger namnet på variabeln.</span><span class="sxs-lookup"><span data-stu-id="5f656-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="5f656-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="5f656-117">-Profile</span></span>
<span data-ttu-id="5f656-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5f656-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f656-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5f656-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f656-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f656-120">CommonParameters</span></span>
<span data-ttu-id="5f656-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f656-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f656-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f656-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f656-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f656-123">INPUTS</span></span>

## <span data-ttu-id="5f656-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f656-124">OUTPUTS</span></span>

## <span data-ttu-id="5f656-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f656-125">NOTES</span></span>

## <span data-ttu-id="5f656-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f656-126">RELATED LINKS</span></span>

[<span data-ttu-id="5f656-127">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5f656-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="5f656-128">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5f656-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="5f656-129">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5f656-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


