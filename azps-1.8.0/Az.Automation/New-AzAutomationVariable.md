---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: ea07e0d0b0c60b35186224d7ea0284df17d1e27b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754784"
---
# <span data-ttu-id="87695-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="87695-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="87695-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87695-102">SYNOPSIS</span></span>
<span data-ttu-id="87695-103">Skapar en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="87695-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="87695-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87695-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87695-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87695-105">DESCRIPTION</span></span>
<span data-ttu-id="87695-106">Cmdleten **New-AzAutomationVariable** skapar en variabel i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="87695-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="87695-107">Om du vill kryptera variabeln anger du den *krypterade* parametern.</span><span class="sxs-lookup"><span data-stu-id="87695-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="87695-108">Du kan inte ändra det krypterade tillståndet för en variabel när du har skapat den.</span><span class="sxs-lookup"><span data-stu-id="87695-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="87695-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87695-109">EXAMPLES</span></span>

### <span data-ttu-id="87695-110">Exempel 1: skapa en variabel med ett enkelt värde</span><span class="sxs-lookup"><span data-stu-id="87695-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="87695-111">Det här kommandot skapar en variabel som heter StringVariable22 med ett sträng värde i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="87695-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="87695-112">Exempel 2: skapa en variabel med ett komplext värde</span><span class="sxs-lookup"><span data-stu-id="87695-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="87695-113">Det första kommandot får en virtuell dator med hjälp av Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87695-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="87695-114">Kommandot sparar det i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="87695-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="87695-115">Det andra kommandot skapar en variabel som heter ComplexVariable01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="87695-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="87695-116">Det här kommandot använder ett komplext objekt för dess värde i det här fallet den virtuella datorn i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="87695-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="87695-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87695-117">PARAMETERS</span></span>

### <span data-ttu-id="87695-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="87695-118">-AutomationAccountName</span></span>
<span data-ttu-id="87695-119">Anger namnet på det Automation-konto där variabeln ska lagras.</span><span class="sxs-lookup"><span data-stu-id="87695-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="87695-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87695-120">-DefaultProfile</span></span>
<span data-ttu-id="87695-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="87695-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87695-122">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="87695-122">-Description</span></span>
<span data-ttu-id="87695-123">Anger en beskrivning av variabeln.</span><span class="sxs-lookup"><span data-stu-id="87695-123">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87695-124">-Krypterade</span><span class="sxs-lookup"><span data-stu-id="87695-124">-Encrypted</span></span>
<span data-ttu-id="87695-125">Anger om denna cmdlet krypterar värdet för variabeln för lagring.</span><span class="sxs-lookup"><span data-stu-id="87695-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87695-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="87695-126">-Name</span></span>
<span data-ttu-id="87695-127">Anger ett namn för variabeln.</span><span class="sxs-lookup"><span data-stu-id="87695-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="87695-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87695-128">-ResourceGroupName</span></span>
<span data-ttu-id="87695-129">Anger den resurs grupp för vilken denna cmdlet skapar en variabel.</span><span class="sxs-lookup"><span data-stu-id="87695-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="87695-130">-Värde</span><span class="sxs-lookup"><span data-stu-id="87695-130">-Value</span></span>
<span data-ttu-id="87695-131">Anger ett värde för variabeln.</span><span class="sxs-lookup"><span data-stu-id="87695-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87695-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87695-132">CommonParameters</span></span>
<span data-ttu-id="87695-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87695-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87695-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87695-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87695-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87695-135">INPUTS</span></span>

### <span data-ttu-id="87695-136">System. String</span><span class="sxs-lookup"><span data-stu-id="87695-136">System.String</span></span>

### <span data-ttu-id="87695-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87695-137">System.Boolean</span></span>

### <span data-ttu-id="87695-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="87695-138">System.Object</span></span>

## <span data-ttu-id="87695-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87695-139">OUTPUTS</span></span>

### <span data-ttu-id="87695-140">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="87695-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="87695-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87695-141">NOTES</span></span>

## <span data-ttu-id="87695-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87695-142">RELATED LINKS</span></span>

[<span data-ttu-id="87695-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="87695-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="87695-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="87695-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="87695-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="87695-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


