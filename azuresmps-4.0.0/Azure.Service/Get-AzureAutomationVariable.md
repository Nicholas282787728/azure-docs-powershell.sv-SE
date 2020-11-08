---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093379"
---
# <span data-ttu-id="1b6a0-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1b6a0-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="1b6a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b6a0-102">SYNOPSIS</span></span>

<span data-ttu-id="1b6a0-103">Hämtar en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="1b6a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b6a0-104">SYNTAX</span></span>

### <span data-ttu-id="1b6a0-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="1b6a0-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1b6a0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1b6a0-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b6a0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b6a0-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1b6a0-108">Cmdleten **Get-AzureAutomationVariable** hämtar en eller flera Microsoft Azure Automation-variabler.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="1b6a0-109">Alla variabler returneras som standard.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-109">By default, all variables are returned.</span></span>
<span data-ttu-id="1b6a0-110">Ange namnet på en viss variabel.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="1b6a0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b6a0-111">EXAMPLES</span></span>

### <span data-ttu-id="1b6a0-112">Exempel 1: få en variabel</span><span class="sxs-lookup"><span data-stu-id="1b6a0-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="1b6a0-113">De här kommandona hämtar en Automation-variabel som heter variabel och tilldelar dess värde till en variabel som kallas $value.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="1b6a0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b6a0-114">PARAMETERS</span></span>

### <span data-ttu-id="1b6a0-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1b6a0-115">-AutomationAccountName</span></span>
<span data-ttu-id="1b6a0-116">Anger namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="1b6a0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b6a0-117">-Name</span></span>
<span data-ttu-id="1b6a0-118">Anger namnet på en variabel.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-118">Specifies the name of a variable.</span></span>

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

### <span data-ttu-id="1b6a0-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="1b6a0-119">-Profile</span></span>
<span data-ttu-id="1b6a0-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1b6a0-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1b6a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6a0-122">CommonParameters</span></span>
<span data-ttu-id="1b6a0-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6a0-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6a0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6a0-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b6a0-125">INPUTS</span></span>

## <span data-ttu-id="1b6a0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b6a0-126">OUTPUTS</span></span>

### <span data-ttu-id="1b6a0-127">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="1b6a0-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="1b6a0-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b6a0-128">NOTES</span></span>

## <span data-ttu-id="1b6a0-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b6a0-129">RELATED LINKS</span></span>

[<span data-ttu-id="1b6a0-130">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1b6a0-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="1b6a0-131">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1b6a0-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="1b6a0-132">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1b6a0-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


