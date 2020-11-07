---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: cc5b347df5f60027ef67ff2bf9d00ad62ca66d6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576338"
---
# <span data-ttu-id="d3616-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d3616-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="d3616-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3616-102">SYNOPSIS</span></span>
<span data-ttu-id="d3616-103">Skapar en automatiserings referens.</span><span class="sxs-lookup"><span data-stu-id="d3616-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3616-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3616-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3616-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3616-105">DESCRIPTION</span></span>
<span data-ttu-id="d3616-106">Cmdleten **New-AzureRmAutomationCredential** skapar en autentiseringsuppgift som ett **PSCredential** -objekt i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d3616-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="d3616-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3616-107">EXAMPLES</span></span>

### <span data-ttu-id="d3616-108">Exempel 1: skapa en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="d3616-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d3616-109">Det första kommandot tilldelar ett användar namn till $User variabel.</span><span class="sxs-lookup"><span data-stu-id="d3616-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="d3616-110">Det andra kommandot konverterar ett oformaterat text lösen ord till en skyddad sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3616-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="d3616-111">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="d3616-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="d3616-112">Det tredje kommandot skapar en autentiseringsuppgift utifrån $User och $Password och lagrar det sedan i $Credential variabeln.</span><span class="sxs-lookup"><span data-stu-id="d3616-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="d3616-113">Med kommandot slut skapas en automatiserings autentiseringsuppgift med namnet ContosoCredential som använder $Credential.</span><span class="sxs-lookup"><span data-stu-id="d3616-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="d3616-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3616-114">PARAMETERS</span></span>

### <span data-ttu-id="d3616-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d3616-115">-AutomationAccountName</span></span>
<span data-ttu-id="d3616-116">Anger namnet på det Automation-konto som denna cmdlet lagrar autentiseringsuppgifterna för.</span><span class="sxs-lookup"><span data-stu-id="d3616-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="d3616-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3616-117">-DefaultProfile</span></span>
<span data-ttu-id="d3616-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d3616-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3616-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d3616-119">-Description</span></span>
<span data-ttu-id="d3616-120">Anger en beskrivning av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="d3616-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="d3616-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3616-121">-Name</span></span>
<span data-ttu-id="d3616-122">Anger ett namn för autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="d3616-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="d3616-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3616-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3616-124">Anger en beskrivning av resurs gruppen som den här cmdleten skapar en autentiseringsuppgift för.</span><span class="sxs-lookup"><span data-stu-id="d3616-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="d3616-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="d3616-125">-Value</span></span>
<span data-ttu-id="d3616-126">Anger autentiseringsuppgifterna som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d3616-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3616-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3616-127">CommonParameters</span></span>
<span data-ttu-id="d3616-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3616-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3616-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3616-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3616-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3616-130">INPUTS</span></span>

### <span data-ttu-id="d3616-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d3616-131">System.String</span></span>

### <span data-ttu-id="d3616-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="d3616-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="d3616-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3616-133">OUTPUTS</span></span>

### <span data-ttu-id="d3616-134">Microsoft. Azure. commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="d3616-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="d3616-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3616-135">NOTES</span></span>

## <span data-ttu-id="d3616-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3616-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3616-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d3616-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="d3616-138">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d3616-138">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="d3616-139">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d3616-139">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)

