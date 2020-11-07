---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 3eecca08264b83ac46b0927273ff07149d4cc348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756640"
---
# <span data-ttu-id="15125-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="15125-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="15125-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15125-102">SYNOPSIS</span></span>
<span data-ttu-id="15125-103">Hämtar en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="15125-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15125-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15125-104">SYNTAX</span></span>

### <span data-ttu-id="15125-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="15125-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15125-106">ByName</span><span class="sxs-lookup"><span data-stu-id="15125-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15125-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15125-107">DESCRIPTION</span></span>
<span data-ttu-id="15125-108">Cmdleten **Get-AzureRmAutomationVariable** hämtar en eller flera Azure Automation-variabler.</span><span class="sxs-lookup"><span data-stu-id="15125-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="15125-109">Ange namnet på en viss variabel.</span><span class="sxs-lookup"><span data-stu-id="15125-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="15125-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15125-110">EXAMPLES</span></span>

### <span data-ttu-id="15125-111">Exempel 1: få en variabel</span><span class="sxs-lookup"><span data-stu-id="15125-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="15125-112">Det första kommandot får en Automation-variabel som heter Variable06 i kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="15125-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="15125-113">Kommandot lagrar objektet i $Variable variabel.</span><span class="sxs-lookup"><span data-stu-id="15125-113">The command stores that object in the $Variable variable.</span></span>

<span data-ttu-id="15125-114">I det andra kommandot används standard punkt notation för att referera till egenskapen **Value** för $Variable.</span><span class="sxs-lookup"><span data-stu-id="15125-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="15125-115">Kommandot lagrar värdet i variabeln $value.</span><span class="sxs-lookup"><span data-stu-id="15125-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="15125-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15125-116">PARAMETERS</span></span>

### <span data-ttu-id="15125-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="15125-117">-AutomationAccountName</span></span>
<span data-ttu-id="15125-118">Anger namnet på det Automation-konto som innehåller de variabler som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="15125-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="15125-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="15125-119">-Name</span></span>
<span data-ttu-id="15125-120">Anger namnet på den variabel som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="15125-120">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="15125-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15125-121">-ResourceGroupName</span></span>
<span data-ttu-id="15125-122">Anger den resurs grupp som den här cmdleten får variabler för.</span><span class="sxs-lookup"><span data-stu-id="15125-122">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="15125-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15125-123">-DefaultProfile</span></span>
<span data-ttu-id="15125-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15125-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15125-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15125-125">CommonParameters</span></span>
<span data-ttu-id="15125-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15125-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15125-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15125-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15125-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15125-128">INPUTS</span></span>

## <span data-ttu-id="15125-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15125-129">OUTPUTS</span></span>

### <span data-ttu-id="15125-130">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="15125-130">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="15125-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15125-131">NOTES</span></span>

## <span data-ttu-id="15125-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15125-132">RELATED LINKS</span></span>

[<span data-ttu-id="15125-133">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="15125-133">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="15125-134">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="15125-134">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="15125-135">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="15125-135">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


