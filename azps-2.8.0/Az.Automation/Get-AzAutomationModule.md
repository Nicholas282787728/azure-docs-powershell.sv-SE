---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 54bbda0226cf2aa374e149bc4b5885b86b31ef12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745566"
---
# <span data-ttu-id="765bb-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="765bb-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="765bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="765bb-102">SYNOPSIS</span></span>
<span data-ttu-id="765bb-103">Hämtar metadata för moduler från Automation.</span><span class="sxs-lookup"><span data-stu-id="765bb-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="765bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="765bb-104">SYNTAX</span></span>

### <span data-ttu-id="765bb-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="765bb-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="765bb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="765bb-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="765bb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="765bb-107">DESCRIPTION</span></span>
<span data-ttu-id="765bb-108">Cmdleten **Get-AzAutomationModule** hämtar metadata för moduler från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="765bb-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="765bb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="765bb-109">EXAMPLES</span></span>

### <span data-ttu-id="765bb-110">Exempel 1: Hämta alla moduler</span><span class="sxs-lookup"><span data-stu-id="765bb-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="765bb-111">Det här kommandot får alla moduler i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="765bb-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="765bb-112">Exempel 2: Hämta en modul</span><span class="sxs-lookup"><span data-stu-id="765bb-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="765bb-113">Det här kommandot hämtar en modul som heter ContosoModule i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="765bb-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="765bb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="765bb-114">PARAMETERS</span></span>

### <span data-ttu-id="765bb-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="765bb-115">-AutomationAccountName</span></span>
<span data-ttu-id="765bb-116">Anger namnet på det Automation-konto som denna cmdlet får modulens metadata för.</span><span class="sxs-lookup"><span data-stu-id="765bb-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="765bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="765bb-117">-DefaultProfile</span></span>
<span data-ttu-id="765bb-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="765bb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="765bb-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="765bb-119">-Name</span></span>
<span data-ttu-id="765bb-120">Anger namnet på den modul där denna cmdlet får metadata.</span><span class="sxs-lookup"><span data-stu-id="765bb-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="765bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="765bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="765bb-122">Anger namnet på en resurs grupp för vilken denna cmdlet får modulens metadata.</span><span class="sxs-lookup"><span data-stu-id="765bb-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="765bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="765bb-123">CommonParameters</span></span>
<span data-ttu-id="765bb-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="765bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="765bb-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="765bb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="765bb-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="765bb-126">INPUTS</span></span>

### <span data-ttu-id="765bb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="765bb-127">System.String</span></span>

## <span data-ttu-id="765bb-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="765bb-128">OUTPUTS</span></span>

### <span data-ttu-id="765bb-129">Microsoft. Azure. commands. Automation. Model. modul</span><span class="sxs-lookup"><span data-stu-id="765bb-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="765bb-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="765bb-130">NOTES</span></span>

## <span data-ttu-id="765bb-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="765bb-131">RELATED LINKS</span></span>

[<span data-ttu-id="765bb-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="765bb-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="765bb-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="765bb-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="765bb-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="765bb-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)

