---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: cb332c1aed8f828f893417561302ddcf36ba0cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578543"
---
# <span data-ttu-id="04385-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04385-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="04385-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04385-102">SYNOPSIS</span></span>
<span data-ttu-id="04385-103">Skapar en automatiserings referens.</span><span class="sxs-lookup"><span data-stu-id="04385-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04385-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04385-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04385-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04385-105">DESCRIPTION</span></span>
<span data-ttu-id="04385-106">Cmdleten **New-AzureRmAutomationCredential** skapar en autentiseringsuppgift som ett **PSCredential** -objekt i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="04385-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="04385-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04385-107">EXAMPLES</span></span>

### <span data-ttu-id="04385-108">Exempel 1: skapa en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="04385-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="04385-109">Det första kommandot tilldelar ett användar namn till $User variabel.</span><span class="sxs-lookup"><span data-stu-id="04385-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="04385-110">Det andra kommandot konverterar ett oformaterat text lösen ord till en skyddad sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04385-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="04385-111">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="04385-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="04385-112">Det tredje kommandot skapar en autentiseringsuppgift utifrån $User och $Password och lagrar det sedan i $Credential variabeln.</span><span class="sxs-lookup"><span data-stu-id="04385-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="04385-113">Med kommandot slut skapas en automatiserings autentiseringsuppgift med namnet ContosoCredential som använder $Credential.</span><span class="sxs-lookup"><span data-stu-id="04385-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="04385-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04385-114">PARAMETERS</span></span>

### <span data-ttu-id="04385-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="04385-115">-AutomationAccountName</span></span>
<span data-ttu-id="04385-116">Anger namnet på det Automation-konto som denna cmdlet lagrar autentiseringsuppgifterna för.</span><span class="sxs-lookup"><span data-stu-id="04385-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="04385-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="04385-117">-Description</span></span>
<span data-ttu-id="04385-118">Anger en beskrivning av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="04385-118">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="04385-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="04385-119">-Name</span></span>
<span data-ttu-id="04385-120">Anger ett namn för autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="04385-120">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="04385-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04385-121">-ResourceGroupName</span></span>
<span data-ttu-id="04385-122">Anger en beskrivning av resurs gruppen som den här cmdleten skapar en autentiseringsuppgift för.</span><span class="sxs-lookup"><span data-stu-id="04385-122">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="04385-123">-Värde</span><span class="sxs-lookup"><span data-stu-id="04385-123">-Value</span></span>
<span data-ttu-id="04385-124">Anger autentiseringsuppgifterna som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="04385-124">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="04385-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04385-125">-DefaultProfile</span></span>
<span data-ttu-id="04385-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04385-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04385-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04385-127">CommonParameters</span></span>
<span data-ttu-id="04385-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04385-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04385-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04385-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04385-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04385-130">INPUTS</span></span>

## <span data-ttu-id="04385-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04385-131">OUTPUTS</span></span>

### <span data-ttu-id="04385-132">Microsoft. Azure. commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="04385-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="04385-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04385-133">NOTES</span></span>

## <span data-ttu-id="04385-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04385-134">RELATED LINKS</span></span>

[<span data-ttu-id="04385-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04385-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="04385-136">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04385-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="04385-137">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04385-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


