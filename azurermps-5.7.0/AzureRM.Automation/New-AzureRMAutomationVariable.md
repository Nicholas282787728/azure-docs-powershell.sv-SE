---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: 217a6553a21871e79998dcad0630f4c0e1b6aec4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583683"
---
# <span data-ttu-id="65dda-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="65dda-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="65dda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65dda-102">SYNOPSIS</span></span>
<span data-ttu-id="65dda-103">Skapar en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="65dda-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65dda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65dda-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65dda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65dda-105">DESCRIPTION</span></span>
<span data-ttu-id="65dda-106">Cmdleten **New-AzureRmAutomationVariable** skapar en variabel i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="65dda-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="65dda-107">Om du vill kryptera variabeln anger du den *krypterade* parametern.</span><span class="sxs-lookup"><span data-stu-id="65dda-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="65dda-108">Du kan inte ändra det krypterade tillståndet för en variabel när du har skapat den.</span><span class="sxs-lookup"><span data-stu-id="65dda-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="65dda-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65dda-109">EXAMPLES</span></span>

### <span data-ttu-id="65dda-110">Exempel 1: skapa en variabel med ett enkelt värde</span><span class="sxs-lookup"><span data-stu-id="65dda-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="65dda-111">Det här kommandot skapar en variabel som heter StringVariable22 med ett sträng värde i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="65dda-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="65dda-112">Exempel 2: skapa en variabel med ett komplext värde</span><span class="sxs-lookup"><span data-stu-id="65dda-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="65dda-113">Det första kommandot får en virtuell dator med hjälp av Get-AzureVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65dda-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="65dda-114">Kommandot sparar det i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="65dda-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="65dda-115">Det andra kommandot skapar en variabel som heter ComplexVariable01 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="65dda-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="65dda-116">Det här kommandot använder ett komplext objekt för dess värde i det här fallet den virtuella datorn i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="65dda-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="65dda-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65dda-117">PARAMETERS</span></span>

### <span data-ttu-id="65dda-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65dda-118">-AutomationAccountName</span></span>
<span data-ttu-id="65dda-119">Anger namnet på det Automation-konto där variabeln ska lagras.</span><span class="sxs-lookup"><span data-stu-id="65dda-119">Specifies the name of the Automation account in which to store the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dda-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65dda-120">-DefaultProfile</span></span>
<span data-ttu-id="65dda-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="65dda-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65dda-122">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="65dda-122">-Description</span></span>
<span data-ttu-id="65dda-123">Anger en beskrivning av variabeln.</span><span class="sxs-lookup"><span data-stu-id="65dda-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="65dda-124">-Krypterade</span><span class="sxs-lookup"><span data-stu-id="65dda-124">-Encrypted</span></span>
<span data-ttu-id="65dda-125">Anger om denna cmdlet krypterar värdet för variabeln för lagring.</span><span class="sxs-lookup"><span data-stu-id="65dda-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="65dda-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="65dda-126">-Name</span></span>
<span data-ttu-id="65dda-127">Anger ett namn för variabeln.</span><span class="sxs-lookup"><span data-stu-id="65dda-127">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dda-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65dda-128">-ResourceGroupName</span></span>
<span data-ttu-id="65dda-129">Anger den resurs grupp för vilken denna cmdlet skapar en variabel.</span><span class="sxs-lookup"><span data-stu-id="65dda-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dda-130">-Värde</span><span class="sxs-lookup"><span data-stu-id="65dda-130">-Value</span></span>
<span data-ttu-id="65dda-131">Anger ett värde för variabeln.</span><span class="sxs-lookup"><span data-stu-id="65dda-131">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="65dda-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65dda-132">CommonParameters</span></span>
<span data-ttu-id="65dda-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65dda-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65dda-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65dda-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65dda-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65dda-135">INPUTS</span></span>

### <span data-ttu-id="65dda-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="65dda-136">None</span></span>
<span data-ttu-id="65dda-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="65dda-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65dda-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65dda-138">OUTPUTS</span></span>

### <span data-ttu-id="65dda-139">Microsoft. Azure. commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="65dda-139">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="65dda-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65dda-140">NOTES</span></span>

## <span data-ttu-id="65dda-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65dda-141">RELATED LINKS</span></span>

[<span data-ttu-id="65dda-142">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="65dda-142">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="65dda-143">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="65dda-143">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="65dda-144">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="65dda-144">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


