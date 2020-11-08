---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090444"
---
# <span data-ttu-id="37a44-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="37a44-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="37a44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37a44-102">SYNOPSIS</span></span>
<span data-ttu-id="37a44-103">Hämtar automatiserings konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="37a44-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="37a44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37a44-104">SYNTAX</span></span>

### <span data-ttu-id="37a44-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="37a44-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37a44-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="37a44-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37a44-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37a44-107">DESCRIPTION</span></span>
<span data-ttu-id="37a44-108">Cmdleten **Get-AzAutomationAccount** får Azure Automation-konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="37a44-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="37a44-109">Mer information om automatiserings konton finns i New-AzAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37a44-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="37a44-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37a44-110">EXAMPLES</span></span>

### <span data-ttu-id="37a44-111">Exempel 1: Hämta alla konton</span><span class="sxs-lookup"><span data-stu-id="37a44-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="37a44-112">Det här kommandot får alla Automation-konton i resurs gruppen som heter ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="37a44-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="37a44-113">Exempel 2: skaffa ett konto</span><span class="sxs-lookup"><span data-stu-id="37a44-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="37a44-114">Det här kommandot får Automation-kontot som heter ContosoAutomationAccount i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="37a44-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="37a44-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37a44-115">PARAMETERS</span></span>

### <span data-ttu-id="37a44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a44-116">-DefaultProfile</span></span>
<span data-ttu-id="37a44-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="37a44-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37a44-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="37a44-118">-Name</span></span>
<span data-ttu-id="37a44-119">Anger namnet på det Automation-konto som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="37a44-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="37a44-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37a44-120">-ResourceGroupName</span></span>
<span data-ttu-id="37a44-121">Anger namnet på en resurs grupp där denna cmdlet ska ha automatiserings konton.</span><span class="sxs-lookup"><span data-stu-id="37a44-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="37a44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a44-122">CommonParameters</span></span>
<span data-ttu-id="37a44-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a44-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37a44-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a44-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37a44-125">INPUTS</span></span>

### <span data-ttu-id="37a44-126">System. String</span><span class="sxs-lookup"><span data-stu-id="37a44-126">System.String</span></span>

## <span data-ttu-id="37a44-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37a44-127">OUTPUTS</span></span>

### <span data-ttu-id="37a44-128">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="37a44-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="37a44-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37a44-129">NOTES</span></span>

## <span data-ttu-id="37a44-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37a44-130">RELATED LINKS</span></span>

[<span data-ttu-id="37a44-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="37a44-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="37a44-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="37a44-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="37a44-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="37a44-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


