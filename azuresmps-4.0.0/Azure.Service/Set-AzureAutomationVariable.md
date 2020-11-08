---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099298"
---
# <span data-ttu-id="c4fdc-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c4fdc-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="c4fdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4fdc-102">SYNOPSIS</span></span>

<span data-ttu-id="c4fdc-103">Ändrar en automatiserings variabel.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="c4fdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4fdc-104">SYNTAX</span></span>

### <span data-ttu-id="c4fdc-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="c4fdc-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c4fdc-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="c4fdc-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c4fdc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4fdc-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c4fdc-108">Cmdleten **set-AzureAutomationVariable** ändrar värdet eller beskrivningen av en variabel i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="c4fdc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4fdc-109">EXAMPLES</span></span>

### <span data-ttu-id="c4fdc-110">Exempel 1: Ange värdet för en variabel</span><span class="sxs-lookup"><span data-stu-id="c4fdc-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="c4fdc-111">Det här kommandot anger ett nytt värde för variabeln som heter MyStringVariable i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c4fdc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4fdc-112">PARAMETERS</span></span>

### <span data-ttu-id="c4fdc-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c4fdc-113">-AutomationAccountName</span></span>
<span data-ttu-id="c4fdc-114">Anger namnet på Automation-kontot med variabeln.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-114">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="c4fdc-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c4fdc-115">-Description</span></span>
<span data-ttu-id="c4fdc-116">Anger en beskrivning av variabeln.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-116">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fdc-117">-Krypterade</span><span class="sxs-lookup"><span data-stu-id="c4fdc-117">-Encrypted</span></span>
<span data-ttu-id="c4fdc-118">Anger om variabeln ska krypteras.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-118">Indicates whether to encrypt the variable.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fdc-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4fdc-119">-Name</span></span>
<span data-ttu-id="c4fdc-120">Anger namnet på variabeln.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-120">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="c4fdc-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4fdc-121">-Profile</span></span>
<span data-ttu-id="c4fdc-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4fdc-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4fdc-124">-Värde</span><span class="sxs-lookup"><span data-stu-id="c4fdc-124">-Value</span></span>
<span data-ttu-id="c4fdc-125">Anger ett värde för variabeln.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-125">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fdc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fdc-126">CommonParameters</span></span>
<span data-ttu-id="c4fdc-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fdc-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4fdc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fdc-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4fdc-129">INPUTS</span></span>

## <span data-ttu-id="c4fdc-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4fdc-130">OUTPUTS</span></span>

### <span data-ttu-id="c4fdc-131">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="c4fdc-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="c4fdc-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4fdc-132">NOTES</span></span>

## <span data-ttu-id="c4fdc-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4fdc-133">RELATED LINKS</span></span>

[<span data-ttu-id="c4fdc-134">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c4fdc-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="c4fdc-135">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c4fdc-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="c4fdc-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c4fdc-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


