---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099451"
---
# <span data-ttu-id="9535e-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9535e-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="9535e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9535e-102">SYNOPSIS</span></span>

<span data-ttu-id="9535e-103">Skapar en autentiseringsuppgift i Automation.</span><span class="sxs-lookup"><span data-stu-id="9535e-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="9535e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9535e-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9535e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9535e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9535e-106">Cmdleten **New-AzureAutomationCredential** skapar en autentiseringsuppgift som ett **PSCredential** -objekt i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9535e-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="9535e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9535e-107">EXAMPLES</span></span>

### <span data-ttu-id="9535e-108">Exempel 1: skapa en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="9535e-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="9535e-109">De här kommandona skapar en autentiseringsuppgift som heter mina autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="9535e-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="9535e-110">Ett objekt med autentiseringsuppgifter skapas först med användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="9535e-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="9535e-111">Detta används sedan i det senaste kommandot för att skapa automatiserings uppgifter.</span><span class="sxs-lookup"><span data-stu-id="9535e-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="9535e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9535e-112">PARAMETERS</span></span>

### <span data-ttu-id="9535e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9535e-113">-AutomationAccountName</span></span>
<span data-ttu-id="9535e-114">Anger namnet på Automation-kontot som autentiseringsuppgiften lagras i.</span><span class="sxs-lookup"><span data-stu-id="9535e-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9535e-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="9535e-115">-Description</span></span>
<span data-ttu-id="9535e-116">Anger en beskrivning av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="9535e-116">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9535e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="9535e-117">-Name</span></span>
<span data-ttu-id="9535e-118">Anger ett namn för autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="9535e-118">Specifies a name for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9535e-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="9535e-119">-Profile</span></span>
<span data-ttu-id="9535e-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="9535e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9535e-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="9535e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9535e-122">-Värde</span><span class="sxs-lookup"><span data-stu-id="9535e-122">-Value</span></span>
<span data-ttu-id="9535e-123">Anger autentiseringsuppgifterna som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9535e-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9535e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9535e-124">CommonParameters</span></span>
<span data-ttu-id="9535e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9535e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9535e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9535e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9535e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9535e-127">INPUTS</span></span>

## <span data-ttu-id="9535e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9535e-128">OUTPUTS</span></span>

### <span data-ttu-id="9535e-129">Microsoft. Azure. commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="9535e-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="9535e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9535e-130">NOTES</span></span>

## <span data-ttu-id="9535e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9535e-131">RELATED LINKS</span></span>

[<span data-ttu-id="9535e-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9535e-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="9535e-133">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9535e-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="9535e-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9535e-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


