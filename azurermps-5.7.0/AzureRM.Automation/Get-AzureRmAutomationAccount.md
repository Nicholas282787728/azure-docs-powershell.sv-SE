---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: 7cddd6ab52774c6ae377ecddb6883d5019d6d7fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758352"
---
# <span data-ttu-id="dba0b-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="dba0b-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="dba0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dba0b-102">SYNOPSIS</span></span>
<span data-ttu-id="dba0b-103">Hämtar automatiserings konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dba0b-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dba0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dba0b-104">SYNTAX</span></span>

### <span data-ttu-id="dba0b-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="dba0b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dba0b-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dba0b-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dba0b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dba0b-107">DESCRIPTION</span></span>
<span data-ttu-id="dba0b-108">Cmdleten **Get-AzureRmAutomationAccount** får Azure Automation-konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dba0b-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="dba0b-109">Mer information om automatiserings konton finns i New-AzureRmAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dba0b-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="dba0b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dba0b-110">EXAMPLES</span></span>

### <span data-ttu-id="dba0b-111">Exempel 1: Hämta alla konton</span><span class="sxs-lookup"><span data-stu-id="dba0b-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="dba0b-112">Det här kommandot får alla Automation-konton i resurs gruppen som heter ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="dba0b-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="dba0b-113">Exempel 2: skaffa ett konto</span><span class="sxs-lookup"><span data-stu-id="dba0b-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="dba0b-114">Det här kommandot får Automation-kontot som heter ContosoAutomationAccount i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dba0b-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="dba0b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dba0b-115">PARAMETERS</span></span>

### <span data-ttu-id="dba0b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba0b-116">-DefaultProfile</span></span>
<span data-ttu-id="dba0b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dba0b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dba0b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="dba0b-118">-Name</span></span>
<span data-ttu-id="dba0b-119">Anger namnet på det Automation-konto som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="dba0b-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dba0b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba0b-120">-ResourceGroupName</span></span>
<span data-ttu-id="dba0b-121">Anger namnet på en resurs grupp där denna cmdlet ska ha automatiserings konton.</span><span class="sxs-lookup"><span data-stu-id="dba0b-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dba0b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba0b-122">CommonParameters</span></span>
<span data-ttu-id="dba0b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba0b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba0b-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba0b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba0b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dba0b-125">INPUTS</span></span>

### <span data-ttu-id="dba0b-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="dba0b-126">None</span></span>
<span data-ttu-id="dba0b-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="dba0b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dba0b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dba0b-128">OUTPUTS</span></span>

### <span data-ttu-id="dba0b-129">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="dba0b-129">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="dba0b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dba0b-130">NOTES</span></span>

## <span data-ttu-id="dba0b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dba0b-131">RELATED LINKS</span></span>

[<span data-ttu-id="dba0b-132">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="dba0b-132">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="dba0b-133">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="dba0b-133">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="dba0b-134">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="dba0b-134">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


