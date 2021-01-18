---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524948"
---
# <span data-ttu-id="1f3a8-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1f3a8-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="1f3a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3a8-103">Hämtar en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="1f3a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f3a8-104">SYNTAX</span></span>

### <span data-ttu-id="1f3a8-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="1f3a8-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f3a8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1f3a8-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f3a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f3a8-107">DESCRIPTION</span></span>
<span data-ttu-id="1f3a8-108">Cmdleten **Get-AzAutomationVariable** hämtar en eller flera Azure Automation-variabler.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="1f3a8-109">Ange namnet på en viss variabel.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="1f3a8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f3a8-110">EXAMPLES</span></span>

### <span data-ttu-id="1f3a8-111">Exempel 1: få en variabel</span><span class="sxs-lookup"><span data-stu-id="1f3a8-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="1f3a8-112">Det första kommandot får en Automation-variabel som heter Variable06 i kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="1f3a8-113">Kommandot lagrar objektet i $Variable variabel.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="1f3a8-114">I det andra kommandot används standard punkt notation för att referera till egenskapen **Value** för $Variable.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="1f3a8-115">Kommandot lagrar värdet i variabeln $value.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="1f3a8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f3a8-116">PARAMETERS</span></span>

### <span data-ttu-id="1f3a8-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f3a8-117">-AutomationAccountName</span></span>
<span data-ttu-id="1f3a8-118">Anger namnet på det Automation-konto som innehåller de variabler som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3a8-119">-DefaultProfile</span></span>
<span data-ttu-id="1f3a8-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1f3a8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f3a8-121">-Name</span></span>
<span data-ttu-id="1f3a8-122">Anger namnet på den variabel som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f3a8-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f3a8-124">Anger den resurs grupp som den här cmdleten får variabler för.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3a8-125">CommonParameters</span></span>
<span data-ttu-id="1f3a8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f3a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3a8-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f3a8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3a8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f3a8-128">INPUTS</span></span>

### <span data-ttu-id="1f3a8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1f3a8-129">System.String</span></span>

## <span data-ttu-id="1f3a8-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f3a8-130">OUTPUTS</span></span>

### <span data-ttu-id="1f3a8-131">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="1f3a8-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="1f3a8-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f3a8-132">NOTES</span></span>

## <span data-ttu-id="1f3a8-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f3a8-133">RELATED LINKS</span></span>

[<span data-ttu-id="1f3a8-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1f3a8-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="1f3a8-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1f3a8-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="1f3a8-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1f3a8-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


