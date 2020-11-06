---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: c2e03cae02c776b69c424ea3ff685a4118ed94bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579836"
---
# <span data-ttu-id="cc5c9-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="cc5c9-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="cc5c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5c9-103">Skapar en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc5c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc5c9-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc5c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc5c9-105">DESCRIPTION</span></span>
<span data-ttu-id="cc5c9-106">Cmdleten **New-AzureRmAutomationVariable** skapar en variabel i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="cc5c9-107">Om du vill kryptera variabeln anger du den *krypterade* parametern.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="cc5c9-108">Du kan inte ändra det krypterade tillståndet för en variabel när du har skapat den.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="cc5c9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc5c9-109">EXAMPLES</span></span>

### <span data-ttu-id="cc5c9-110">Exempel 1: skapa en variabel med ett enkelt värde</span><span class="sxs-lookup"><span data-stu-id="cc5c9-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cc5c9-111">Det här kommandot skapar en variabel som heter StringVariable22 med ett sträng värde i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cc5c9-112">Exempel 2: skapa en variabel med ett komplext värde</span><span class="sxs-lookup"><span data-stu-id="cc5c9-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cc5c9-113">Det första kommandot får en virtuell dator med hjälp av Get-AzureVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="cc5c9-114">Kommandot sparar det i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="cc5c9-115">Det andra kommandot skapar en variabel som heter ComplexVariable01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="cc5c9-116">Det här kommandot använder ett komplext objekt för dess värde i det här fallet den virtuella datorn i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="cc5c9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc5c9-117">PARAMETERS</span></span>

### <span data-ttu-id="cc5c9-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cc5c9-118">-AutomationAccountName</span></span>
<span data-ttu-id="cc5c9-119">Anger namnet på det Automation-konto där variabeln ska lagras.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="cc5c9-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="cc5c9-120">-Description</span></span>
<span data-ttu-id="cc5c9-121">Anger en beskrivning av variabeln.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="cc5c9-122">-Krypterade</span><span class="sxs-lookup"><span data-stu-id="cc5c9-122">-Encrypted</span></span>
<span data-ttu-id="cc5c9-123">Anger om denna cmdlet krypterar värdet för variabeln för lagring.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-123">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="cc5c9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc5c9-124">-Name</span></span>
<span data-ttu-id="cc5c9-125">Anger ett namn för variabeln.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-125">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="cc5c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc5c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="cc5c9-127">Anger den resurs grupp för vilken denna cmdlet skapar en variabel.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-127">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="cc5c9-128">-Värde</span><span class="sxs-lookup"><span data-stu-id="cc5c9-128">-Value</span></span>
<span data-ttu-id="cc5c9-129">Anger ett värde för variabeln.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="cc5c9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5c9-130">-DefaultProfile</span></span>
<span data-ttu-id="cc5c9-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc5c9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5c9-132">CommonParameters</span></span>
<span data-ttu-id="cc5c9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc5c9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5c9-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc5c9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5c9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc5c9-135">INPUTS</span></span>

## <span data-ttu-id="cc5c9-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc5c9-136">OUTPUTS</span></span>

### <span data-ttu-id="cc5c9-137">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="cc5c9-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="cc5c9-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc5c9-138">NOTES</span></span>

## <span data-ttu-id="cc5c9-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc5c9-139">RELATED LINKS</span></span>

[<span data-ttu-id="cc5c9-140">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="cc5c9-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="cc5c9-141">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="cc5c9-141">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="cc5c9-142">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="cc5c9-142">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


