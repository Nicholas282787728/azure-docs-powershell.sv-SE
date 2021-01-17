---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418272"
---
# <span data-ttu-id="87022-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="87022-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="87022-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87022-102">SYNOPSIS</span></span>
<span data-ttu-id="87022-103">Ändrar en automatiserings autentiseringsuppgift.</span><span class="sxs-lookup"><span data-stu-id="87022-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="87022-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87022-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87022-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87022-105">DESCRIPTION</span></span>
<span data-ttu-id="87022-106">Cmdleten **set-AzAutomationCredential** ändrar en autentiseringsuppgift som ett **PSCredential** -objekt i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="87022-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="87022-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87022-107">EXAMPLES</span></span>

### <span data-ttu-id="87022-108">Exempel 1: uppdatera en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="87022-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="87022-109">Det första kommandot tilldelar ett användar namn till $User variabel.</span><span class="sxs-lookup"><span data-stu-id="87022-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="87022-110">Det andra kommandot konverterar ett oformaterat text lösen ord till en skyddad sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87022-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="87022-111">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="87022-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="87022-112">Det tredje kommandot skapar en autentiseringsuppgift utifrån $User och $Password och lagrar det sedan i $Credential variabeln.</span><span class="sxs-lookup"><span data-stu-id="87022-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="87022-113">Det slutliga kommandot ändrar den Automation-autentiseringsuppgift som heter ContosoCredential att använda autentiseringsuppgiften i $Credential.</span><span class="sxs-lookup"><span data-stu-id="87022-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="87022-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87022-114">PARAMETERS</span></span>

### <span data-ttu-id="87022-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="87022-115">-AutomationAccountName</span></span>
<span data-ttu-id="87022-116">Anger namnet på det Automation-konto som denna cmdlet ändrar en autentiseringsuppgift för.</span><span class="sxs-lookup"><span data-stu-id="87022-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="87022-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87022-117">-DefaultProfile</span></span>
<span data-ttu-id="87022-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="87022-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87022-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="87022-119">-Description</span></span>
<span data-ttu-id="87022-120">Anger en beskrivning av den autentiseringsuppgift som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="87022-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="87022-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="87022-121">-Name</span></span>
<span data-ttu-id="87022-122">Anger namnet på den autentiseringsuppgift som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="87022-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="87022-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87022-123">-ResourceGroupName</span></span>
<span data-ttu-id="87022-124">Anger namnet på den resurs grupp som den här cmdleten ändrar en autentiseringsuppgift för.</span><span class="sxs-lookup"><span data-stu-id="87022-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="87022-125">-Värde</span><span class="sxs-lookup"><span data-stu-id="87022-125">-Value</span></span>
<span data-ttu-id="87022-126">Anger autentiseringsuppgifterna som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="87022-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87022-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87022-127">CommonParameters</span></span>
<span data-ttu-id="87022-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87022-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87022-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87022-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87022-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87022-130">INPUTS</span></span>

### <span data-ttu-id="87022-131">System. String</span><span class="sxs-lookup"><span data-stu-id="87022-131">System.String</span></span>

### <span data-ttu-id="87022-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="87022-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="87022-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87022-133">OUTPUTS</span></span>

### <span data-ttu-id="87022-134">Microsoft. Azure. commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="87022-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="87022-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87022-135">NOTES</span></span>

## <span data-ttu-id="87022-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87022-136">RELATED LINKS</span></span>

[<span data-ttu-id="87022-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="87022-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="87022-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="87022-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="87022-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="87022-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


