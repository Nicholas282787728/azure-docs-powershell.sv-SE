---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099161"
---
# <span data-ttu-id="0771a-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0771a-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="0771a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0771a-102">SYNOPSIS</span></span>

<span data-ttu-id="0771a-103">Skapar en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="0771a-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="0771a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0771a-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0771a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0771a-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0771a-106">Cmdleten **New-AzureAutomationVariable** skapar en variabel i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0771a-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="0771a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0771a-107">EXAMPLES</span></span>

### <span data-ttu-id="0771a-108">Exempel 1: skapa en ny variabel med ett enkelt värde</span><span class="sxs-lookup"><span data-stu-id="0771a-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="0771a-109">Det här kommandot skapar en ny variabel som heter MyStringVariable med ett sträng värde i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0771a-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="0771a-110">Exempel 2: skapa en ny variabel med ett komplext värde</span><span class="sxs-lookup"><span data-stu-id="0771a-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="0771a-111">De här kommandona skapar en ny variabel med namnet MyComplexVariable i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0771a-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="0771a-112">Ett komplext objekt används för dess värde i det här fallet ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="0771a-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="0771a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0771a-113">PARAMETERS</span></span>

### <span data-ttu-id="0771a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0771a-114">-AutomationAccountName</span></span>
<span data-ttu-id="0771a-115">Anger namnet på Automation-kontot som variabeln kommer att lagras i.</span><span class="sxs-lookup"><span data-stu-id="0771a-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

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

### <span data-ttu-id="0771a-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="0771a-116">-Description</span></span>
<span data-ttu-id="0771a-117">Anger en beskrivning av variabeln.</span><span class="sxs-lookup"><span data-stu-id="0771a-117">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="0771a-118">-Krypterade</span><span class="sxs-lookup"><span data-stu-id="0771a-118">-Encrypted</span></span>
<span data-ttu-id="0771a-119">Anger om variabelns värde ska vara krypterat.</span><span class="sxs-lookup"><span data-stu-id="0771a-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0771a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0771a-120">-Name</span></span>
<span data-ttu-id="0771a-121">Anger ett namn för variabeln.</span><span class="sxs-lookup"><span data-stu-id="0771a-121">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="0771a-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="0771a-122">-Profile</span></span>
<span data-ttu-id="0771a-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0771a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0771a-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0771a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0771a-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="0771a-125">-Value</span></span>
<span data-ttu-id="0771a-126">Anger ett värde som ska lagras i variabeln.</span><span class="sxs-lookup"><span data-stu-id="0771a-126">Specifies a value to store in the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0771a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0771a-127">CommonParameters</span></span>
<span data-ttu-id="0771a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0771a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0771a-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0771a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0771a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0771a-130">INPUTS</span></span>

## <span data-ttu-id="0771a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0771a-131">OUTPUTS</span></span>

### <span data-ttu-id="0771a-132">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="0771a-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="0771a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0771a-133">NOTES</span></span>

## <span data-ttu-id="0771a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0771a-134">RELATED LINKS</span></span>

[<span data-ttu-id="0771a-135">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0771a-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="0771a-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0771a-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="0771a-137">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0771a-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


