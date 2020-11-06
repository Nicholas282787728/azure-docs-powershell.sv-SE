---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: a72b7dcb729df3327277b2156574c5a0d5d9deb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573004"
---
# <span data-ttu-id="57b6a-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="57b6a-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="57b6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="57b6a-103">Hämtar automatiserings konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="57b6a-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57b6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57b6a-104">SYNTAX</span></span>

### <span data-ttu-id="57b6a-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="57b6a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57b6a-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="57b6a-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57b6a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57b6a-107">DESCRIPTION</span></span>
<span data-ttu-id="57b6a-108">Cmdleten **Get-AzureRmAutomationAccount** får Azure Automation-konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="57b6a-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="57b6a-109">Mer information om automatiserings konton finns i New-AzureRmAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b6a-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="57b6a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57b6a-110">EXAMPLES</span></span>

### <span data-ttu-id="57b6a-111">Exempel 1: Hämta alla konton</span><span class="sxs-lookup"><span data-stu-id="57b6a-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="57b6a-112">Det här kommandot får alla Automation-konton i resurs gruppen som heter ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="57b6a-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="57b6a-113">Exempel 2: skaffa ett konto</span><span class="sxs-lookup"><span data-stu-id="57b6a-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="57b6a-114">Det här kommandot får Automation-kontot som heter ContosoAutomationAccount i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="57b6a-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="57b6a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57b6a-115">PARAMETERS</span></span>

### <span data-ttu-id="57b6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b6a-116">-DefaultProfile</span></span>
<span data-ttu-id="57b6a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="57b6a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57b6a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="57b6a-118">-Name</span></span>
<span data-ttu-id="57b6a-119">Anger namnet på det Automation-konto som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="57b6a-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="57b6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b6a-120">-ResourceGroupName</span></span>
<span data-ttu-id="57b6a-121">Anger namnet på en resurs grupp där denna cmdlet ska ha automatiserings konton.</span><span class="sxs-lookup"><span data-stu-id="57b6a-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="57b6a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b6a-122">CommonParameters</span></span>
<span data-ttu-id="57b6a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b6a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b6a-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57b6a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b6a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57b6a-125">INPUTS</span></span>

### <span data-ttu-id="57b6a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="57b6a-126">System.String</span></span>

## <span data-ttu-id="57b6a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57b6a-127">OUTPUTS</span></span>

### <span data-ttu-id="57b6a-128">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="57b6a-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="57b6a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57b6a-129">NOTES</span></span>

## <span data-ttu-id="57b6a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57b6a-130">RELATED LINKS</span></span>

[<span data-ttu-id="57b6a-131">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="57b6a-131">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="57b6a-132">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="57b6a-132">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="57b6a-133">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="57b6a-133">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


