---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: e2a461666edf4f06e78f2bc97f47fcb63ab1c19a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575044"
---
# <span data-ttu-id="a088f-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a088f-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="a088f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a088f-102">SYNOPSIS</span></span>
<span data-ttu-id="a088f-103">Ändrar en automatiserings autentiseringsuppgift.</span><span class="sxs-lookup"><span data-stu-id="a088f-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a088f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a088f-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a088f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a088f-105">DESCRIPTION</span></span>
<span data-ttu-id="a088f-106">Cmdleten **set-AzureRmAutomationCredential** ändrar en autentiseringsuppgift som ett **PSCredential** -objekt i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a088f-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="a088f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a088f-107">EXAMPLES</span></span>

### <span data-ttu-id="a088f-108">Exempel 1: uppdatera en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="a088f-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="a088f-109">Det första kommandot tilldelar ett användar namn till $User variabel.</span><span class="sxs-lookup"><span data-stu-id="a088f-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="a088f-110">Det andra kommandot konverterar ett oformaterat text lösen ord till en skyddad sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a088f-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="a088f-111">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="a088f-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="a088f-112">Det tredje kommandot skapar en autentiseringsuppgift utifrån $User och $Password och lagrar det sedan i $Credential variabeln.</span><span class="sxs-lookup"><span data-stu-id="a088f-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="a088f-113">Det slutliga kommandot ändrar den Automation-autentiseringsuppgift som heter ContosoCredential att använda autentiseringsuppgiften i $Credential.</span><span class="sxs-lookup"><span data-stu-id="a088f-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="a088f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a088f-114">PARAMETERS</span></span>

### <span data-ttu-id="a088f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a088f-115">-AutomationAccountName</span></span>
<span data-ttu-id="a088f-116">Anger namnet på det Automation-konto som denna cmdlet ändrar en autentiseringsuppgift för.</span><span class="sxs-lookup"><span data-stu-id="a088f-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="a088f-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a088f-117">-Description</span></span>
<span data-ttu-id="a088f-118">Anger en beskrivning av den autentiseringsuppgift som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a088f-118">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a088f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a088f-119">-Name</span></span>
<span data-ttu-id="a088f-120">Anger namnet på den autentiseringsuppgift som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="a088f-120">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a088f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a088f-121">-ResourceGroupName</span></span>
<span data-ttu-id="a088f-122">Anger namnet på den resurs grupp som den här cmdleten ändrar en autentiseringsuppgift för.</span><span class="sxs-lookup"><span data-stu-id="a088f-122">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="a088f-123">-Värde</span><span class="sxs-lookup"><span data-stu-id="a088f-123">-Value</span></span>
<span data-ttu-id="a088f-124">Anger autentiseringsuppgifterna som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a088f-124">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="a088f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a088f-125">-DefaultProfile</span></span>
<span data-ttu-id="a088f-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a088f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a088f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a088f-127">CommonParameters</span></span>
<span data-ttu-id="a088f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a088f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a088f-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a088f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a088f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a088f-130">INPUTS</span></span>

## <span data-ttu-id="a088f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a088f-131">OUTPUTS</span></span>

### <span data-ttu-id="a088f-132">Microsoft. Azure. commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="a088f-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="a088f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a088f-133">NOTES</span></span>

## <span data-ttu-id="a088f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a088f-134">RELATED LINKS</span></span>

[<span data-ttu-id="a088f-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a088f-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="a088f-136">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a088f-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="a088f-137">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a088f-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


