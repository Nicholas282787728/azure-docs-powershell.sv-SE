---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927929"
---
# <span data-ttu-id="96568-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="96568-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="96568-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96568-102">SYNOPSIS</span></span>
<span data-ttu-id="96568-103">Ändrar en automatiserings variabel.</span><span class="sxs-lookup"><span data-stu-id="96568-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="96568-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96568-104">SYNTAX</span></span>

### <span data-ttu-id="96568-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="96568-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96568-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="96568-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96568-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96568-107">DESCRIPTION</span></span>
<span data-ttu-id="96568-108">Cmdleten **set-AzAutomationVariable** ändrar värdet eller beskrivningen av en variabel i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="96568-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="96568-109">Om du vill kryptera variabeln anger du den *krypterade* parametern.</span><span class="sxs-lookup"><span data-stu-id="96568-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="96568-110">Du kan inte ändra det krypterade tillståndet för en variabel när du har skapat den.</span><span class="sxs-lookup"><span data-stu-id="96568-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="96568-111">Det går inte att ange *krypterade* för en befintlig, icke-krypterad variabel.</span><span class="sxs-lookup"><span data-stu-id="96568-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="96568-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96568-112">EXAMPLES</span></span>

### <span data-ttu-id="96568-113">Exempel 1: Ange värdet för en variabel</span><span class="sxs-lookup"><span data-stu-id="96568-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="96568-114">Det här kommandot anger ett nytt värde för variabeln som heter StringVariable22 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="96568-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="96568-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96568-115">PARAMETERS</span></span>

### <span data-ttu-id="96568-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="96568-116">-AutomationAccountName</span></span>
<span data-ttu-id="96568-117">Anger namnet på det Automation-konto där variabeln lagras.</span><span class="sxs-lookup"><span data-stu-id="96568-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="96568-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96568-118">-DefaultProfile</span></span>
<span data-ttu-id="96568-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="96568-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96568-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="96568-120">-Description</span></span>
<span data-ttu-id="96568-121">Anger en beskrivning av variabeln.</span><span class="sxs-lookup"><span data-stu-id="96568-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96568-122">-Krypterade</span><span class="sxs-lookup"><span data-stu-id="96568-122">-Encrypted</span></span>
<span data-ttu-id="96568-123">Anger om cmdlet krypterar variabelns värde för lagring.</span><span class="sxs-lookup"><span data-stu-id="96568-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96568-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="96568-124">-Name</span></span>
<span data-ttu-id="96568-125">Anger namnet på den variabel som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="96568-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96568-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96568-126">-ResourceGroupName</span></span>
<span data-ttu-id="96568-127">Anger den resurs grupp för vilken denna cmdlet ändrar en variabel.</span><span class="sxs-lookup"><span data-stu-id="96568-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="96568-128">-Värde</span><span class="sxs-lookup"><span data-stu-id="96568-128">-Value</span></span>
<span data-ttu-id="96568-129">Anger ett värde för variabeln.</span><span class="sxs-lookup"><span data-stu-id="96568-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96568-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96568-130">CommonParameters</span></span>
<span data-ttu-id="96568-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96568-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96568-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96568-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96568-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96568-133">INPUTS</span></span>

### <span data-ttu-id="96568-134">System. String</span><span class="sxs-lookup"><span data-stu-id="96568-134">System.String</span></span>

### <span data-ttu-id="96568-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96568-135">System.Boolean</span></span>

### <span data-ttu-id="96568-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="96568-136">System.Object</span></span>

## <span data-ttu-id="96568-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96568-137">OUTPUTS</span></span>

### <span data-ttu-id="96568-138">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="96568-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="96568-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96568-139">NOTES</span></span>

## <span data-ttu-id="96568-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96568-140">RELATED LINKS</span></span>

[<span data-ttu-id="96568-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="96568-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="96568-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="96568-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="96568-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="96568-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


