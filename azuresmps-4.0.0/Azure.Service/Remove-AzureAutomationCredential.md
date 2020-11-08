---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099710"
---
# <span data-ttu-id="aabba-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="aabba-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="aabba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aabba-102">SYNOPSIS</span></span>

<span data-ttu-id="aabba-103">Tar bort en autentiseringsuppgift från Automation.</span><span class="sxs-lookup"><span data-stu-id="aabba-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="aabba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aabba-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aabba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aabba-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="aabba-106">Cmdleten **Remove-AzureAutomationCredential** tar bort en autentiseringsuppgift från Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="aabba-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="aabba-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aabba-107">EXAMPLES</span></span>

### <span data-ttu-id="aabba-108">Exempel 1: ta bort en autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="aabba-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="aabba-109">Det här kommandot tar bort en autentiseringsuppgift som heter mina autentiseringsuppgifter i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="aabba-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="aabba-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aabba-110">PARAMETERS</span></span>

### <span data-ttu-id="aabba-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aabba-111">-AutomationAccountName</span></span>
<span data-ttu-id="aabba-112">Anger namnet på Automation-kontot med autentiseringsuppgiften.</span><span class="sxs-lookup"><span data-stu-id="aabba-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="aabba-113">-Force</span><span class="sxs-lookup"><span data-stu-id="aabba-113">-Force</span></span>
<span data-ttu-id="aabba-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="aabba-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabba-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="aabba-115">-Name</span></span>
<span data-ttu-id="aabba-116">Anger namnet på den autentiseringsuppgift som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="aabba-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="aabba-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="aabba-117">-Profile</span></span>
<span data-ttu-id="aabba-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="aabba-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aabba-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="aabba-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aabba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabba-120">CommonParameters</span></span>
<span data-ttu-id="aabba-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aabba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabba-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aabba-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabba-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aabba-123">INPUTS</span></span>

## <span data-ttu-id="aabba-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aabba-124">OUTPUTS</span></span>

## <span data-ttu-id="aabba-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aabba-125">NOTES</span></span>

## <span data-ttu-id="aabba-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aabba-126">RELATED LINKS</span></span>

[<span data-ttu-id="aabba-127">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="aabba-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="aabba-128">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="aabba-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="aabba-129">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="aabba-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


