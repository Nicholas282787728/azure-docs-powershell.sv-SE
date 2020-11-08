---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C92B4B70-4342-4219-80D3-FB79BDC171A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16fbdf1a0a63fb5a75aa7bc200036a7332ea15f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099061"
---
# <span data-ttu-id="11b94-101">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="11b94-101">Set-AzureAutomationCredential</span></span>

## <span data-ttu-id="11b94-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11b94-102">SYNOPSIS</span></span>

<span data-ttu-id="11b94-103">Ändrar en autentiseringsuppgift i Automation.</span><span class="sxs-lookup"><span data-stu-id="11b94-103">Modifies a credential in Automation.</span></span>

## <span data-ttu-id="11b94-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11b94-104">SYNTAX</span></span>

```
Set-AzureAutomationCredential -Name <String> [-Description <String>] [-Value <PSCredential>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="11b94-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11b94-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="11b94-106">Cmdleten **set-AzureAutomationCredential** ändrar en autentiseringsuppgift som ett **PSCredential** -objekt i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="11b94-106">The **Set-AzureAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="11b94-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11b94-107">EXAMPLES</span></span>

### <span data-ttu-id="11b94-108">Exempel 1: uppdatera en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="11b94-108">Example 1: Update a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contos17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="11b94-109">Dessa kommandon uppdaterar en befintlig autentiseringsuppgift som heter mina autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="11b94-109">These commands update an existing credential named MyCredential.</span></span>
<span data-ttu-id="11b94-110">Ett objekt med autentiseringsuppgifter skapas först med användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="11b94-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="11b94-111">Detta används sedan i det senaste kommandot för att uppdatera automatiserings referensen.</span><span class="sxs-lookup"><span data-stu-id="11b94-111">This is then used in the last command to update the automation credential.</span></span>

## <span data-ttu-id="11b94-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11b94-112">PARAMETERS</span></span>

### <span data-ttu-id="11b94-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="11b94-113">-AutomationAccountName</span></span>
<span data-ttu-id="11b94-114">Anger namnet på Automation-kontot med autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="11b94-114">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="11b94-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="11b94-115">-Description</span></span>
<span data-ttu-id="11b94-116">Anger en beskrivning av autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="11b94-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="11b94-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="11b94-117">-Name</span></span>
<span data-ttu-id="11b94-118">Anger namnet på autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="11b94-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="11b94-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="11b94-119">-Profile</span></span>
<span data-ttu-id="11b94-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="11b94-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="11b94-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="11b94-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11b94-122">-Värde</span><span class="sxs-lookup"><span data-stu-id="11b94-122">-Value</span></span>
<span data-ttu-id="11b94-123">Anger autentiseringsuppgifterna som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="11b94-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b94-124">CommonParameters</span></span>
<span data-ttu-id="11b94-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b94-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b94-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b94-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11b94-127">INPUTS</span></span>

## <span data-ttu-id="11b94-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11b94-128">OUTPUTS</span></span>

### <span data-ttu-id="11b94-129">Microsoft. Azure. commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="11b94-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="11b94-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11b94-130">NOTES</span></span>

## <span data-ttu-id="11b94-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11b94-131">RELATED LINKS</span></span>

[<span data-ttu-id="11b94-132">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="11b94-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="11b94-133">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="11b94-133">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="11b94-134">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="11b94-134">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)


