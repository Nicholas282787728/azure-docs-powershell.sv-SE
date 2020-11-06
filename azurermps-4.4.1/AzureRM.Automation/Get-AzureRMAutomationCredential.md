---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: f00cbe95c71bdbd8c7f92f123756fa0c474d878f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586267"
---
# <span data-ttu-id="4e010-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4e010-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="4e010-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e010-102">SYNOPSIS</span></span>
<span data-ttu-id="4e010-103">Får automatiserings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="4e010-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e010-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e010-104">SYNTAX</span></span>

### <span data-ttu-id="4e010-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="4e010-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e010-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4e010-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e010-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e010-107">DESCRIPTION</span></span>
<span data-ttu-id="4e010-108">Cmdleten **Get-AzureRmAutomationCredential** får en eller flera Azure Automation-autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="4e010-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="4e010-109">Som standard returneras alla autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="4e010-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="4e010-110">Ange namnet på en autentiseringsuppgift för att få en viss autentiseringsuppgift.</span><span class="sxs-lookup"><span data-stu-id="4e010-110">Specify the name of a credential to get a specific credential.</span></span>

<span data-ttu-id="4e010-111">Av säkerhets skäl går det inte att returnera lösen ord för inloggning.</span><span class="sxs-lookup"><span data-stu-id="4e010-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="4e010-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e010-112">EXAMPLES</span></span>

### <span data-ttu-id="4e010-113">Exempel 1: Hämta alla autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="4e010-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="4e010-114">Det här kommandot får metadata för alla autentiseringsuppgifter i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4e010-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4e010-115">Exempel 2: skaffa en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="4e010-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="4e010-116">Det här kommandot får metadata för autentiseringsuppgifterna som heter ContosoCredential i Automation-kontot med Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4e010-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4e010-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e010-117">PARAMETERS</span></span>

### <span data-ttu-id="4e010-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e010-118">-AutomationAccountName</span></span>
<span data-ttu-id="4e010-119">Anger namnet på det Automation-konto som denna cmdlet hämtar autentiseringsuppgifter för.</span><span class="sxs-lookup"><span data-stu-id="4e010-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="4e010-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e010-120">-Name</span></span>
<span data-ttu-id="4e010-121">Anger namnet på en autentiseringsuppgift som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="4e010-121">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="4e010-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e010-122">-ResourceGroupName</span></span>
<span data-ttu-id="4e010-123">Anger den resurs grupp för vilken denna cmdlet hämtar autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="4e010-123">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="4e010-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e010-124">-DefaultProfile</span></span>
<span data-ttu-id="4e010-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e010-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e010-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e010-126">CommonParameters</span></span>
<span data-ttu-id="4e010-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e010-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e010-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e010-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e010-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e010-129">INPUTS</span></span>

## <span data-ttu-id="4e010-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e010-130">OUTPUTS</span></span>

### <span data-ttu-id="4e010-131">Microsoft. Azure. commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="4e010-131">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="4e010-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e010-132">NOTES</span></span>

## <span data-ttu-id="4e010-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e010-133">RELATED LINKS</span></span>

[<span data-ttu-id="4e010-134">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4e010-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="4e010-135">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4e010-135">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="4e010-136">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4e010-136">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


