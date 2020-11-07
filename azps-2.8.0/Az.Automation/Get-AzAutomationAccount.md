---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 6c5e0a376b8170c73abc394f275995b178e90917
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745602"
---
# <span data-ttu-id="1f2cf-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1f2cf-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="1f2cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="1f2cf-103">Hämtar automatiserings konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1f2cf-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="1f2cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f2cf-104">SYNTAX</span></span>

### <span data-ttu-id="1f2cf-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="1f2cf-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f2cf-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f2cf-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f2cf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f2cf-107">DESCRIPTION</span></span>
<span data-ttu-id="1f2cf-108">Cmdleten **Get-AzAutomationAccount** får Azure Automation-konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1f2cf-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="1f2cf-109">Mer information om automatiserings konton finns i New-AzAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f2cf-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="1f2cf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f2cf-110">EXAMPLES</span></span>

### <span data-ttu-id="1f2cf-111">Exempel 1: Hämta alla konton</span><span class="sxs-lookup"><span data-stu-id="1f2cf-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="1f2cf-112">Det här kommandot får alla Automation-konton i resurs gruppen som heter ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="1f2cf-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="1f2cf-113">Exempel 2: skaffa ett konto</span><span class="sxs-lookup"><span data-stu-id="1f2cf-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="1f2cf-114">Det här kommandot får Automation-kontot som heter ContosoAutomationAccount i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f2cf-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="1f2cf-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f2cf-115">PARAMETERS</span></span>

### <span data-ttu-id="1f2cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f2cf-116">-DefaultProfile</span></span>
<span data-ttu-id="1f2cf-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1f2cf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f2cf-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f2cf-118">-Name</span></span>
<span data-ttu-id="1f2cf-119">Anger namnet på det Automation-konto som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="1f2cf-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f2cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f2cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f2cf-121">Anger namnet på en resurs grupp där denna cmdlet ska ha automatiserings konton.</span><span class="sxs-lookup"><span data-stu-id="1f2cf-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f2cf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f2cf-122">CommonParameters</span></span>
<span data-ttu-id="1f2cf-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f2cf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f2cf-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f2cf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f2cf-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f2cf-125">INPUTS</span></span>

### <span data-ttu-id="1f2cf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1f2cf-126">System.String</span></span>

## <span data-ttu-id="1f2cf-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f2cf-127">OUTPUTS</span></span>

### <span data-ttu-id="1f2cf-128">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1f2cf-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="1f2cf-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f2cf-129">NOTES</span></span>

## <span data-ttu-id="1f2cf-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f2cf-130">RELATED LINKS</span></span>

[<span data-ttu-id="1f2cf-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1f2cf-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="1f2cf-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1f2cf-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="1f2cf-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1f2cf-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


