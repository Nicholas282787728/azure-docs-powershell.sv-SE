---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092697"
---
# <span data-ttu-id="ab6df-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ab6df-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="ab6df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab6df-102">SYNOPSIS</span></span>
<span data-ttu-id="ab6df-103">Skapar en automatiserings referens.</span><span class="sxs-lookup"><span data-stu-id="ab6df-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="ab6df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab6df-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab6df-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab6df-105">DESCRIPTION</span></span>
<span data-ttu-id="ab6df-106">Cmdleten **New-AzAutomationCredential** skapar en autentiseringsuppgift som ett **PSCredential** -objekt i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ab6df-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="ab6df-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab6df-107">EXAMPLES</span></span>

### <span data-ttu-id="ab6df-108">Exempel 1: skapa en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="ab6df-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ab6df-109">Det första kommandot tilldelar ett användar namn till $User variabel.</span><span class="sxs-lookup"><span data-stu-id="ab6df-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="ab6df-110">Det andra kommandot konverterar ett oformaterat text lösen ord till en skyddad sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab6df-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="ab6df-111">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="ab6df-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="ab6df-112">Det tredje kommandot skapar en autentiseringsuppgift utifrån $User och $Password och lagrar det sedan i $Credential variabeln.</span><span class="sxs-lookup"><span data-stu-id="ab6df-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="ab6df-113">Med kommandot slut skapas en automatiserings autentiseringsuppgift med namnet ContosoCredential som använder $Credential.</span><span class="sxs-lookup"><span data-stu-id="ab6df-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="ab6df-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab6df-114">PARAMETERS</span></span>

### <span data-ttu-id="ab6df-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ab6df-115">-AutomationAccountName</span></span>
<span data-ttu-id="ab6df-116">Anger namnet på det Automation-konto som denna cmdlet lagrar autentiseringsuppgifterna för.</span><span class="sxs-lookup"><span data-stu-id="ab6df-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="ab6df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab6df-117">-DefaultProfile</span></span>
<span data-ttu-id="ab6df-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ab6df-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab6df-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ab6df-119">-Description</span></span>
<span data-ttu-id="ab6df-120">Anger en beskrivning av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="ab6df-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="ab6df-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab6df-121">-Name</span></span>
<span data-ttu-id="ab6df-122">Anger ett namn för autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="ab6df-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="ab6df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab6df-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab6df-124">Anger en beskrivning av resurs gruppen som den här cmdleten skapar en autentiseringsuppgift för.</span><span class="sxs-lookup"><span data-stu-id="ab6df-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="ab6df-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="ab6df-125">-Value</span></span>
<span data-ttu-id="ab6df-126">Anger autentiseringsuppgifterna som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ab6df-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="ab6df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab6df-127">CommonParameters</span></span>
<span data-ttu-id="ab6df-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab6df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab6df-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab6df-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab6df-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab6df-130">INPUTS</span></span>

### <span data-ttu-id="ab6df-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ab6df-131">System.String</span></span>

### <span data-ttu-id="ab6df-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="ab6df-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="ab6df-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab6df-133">OUTPUTS</span></span>

### <span data-ttu-id="ab6df-134">Microsoft. Azure. commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="ab6df-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="ab6df-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab6df-135">NOTES</span></span>

## <span data-ttu-id="ab6df-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab6df-136">RELATED LINKS</span></span>

[<span data-ttu-id="ab6df-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ab6df-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="ab6df-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ab6df-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="ab6df-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="ab6df-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)

